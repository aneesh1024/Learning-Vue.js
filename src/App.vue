<template>
  <div>
    <div>{{ greet }} {{ name }}</div> <!-- 1st way to add dynamic text by using the mustache syntax -->
    <div v-html="hack"></div> <!-- 2nd way is by using v-bind director  -->
    <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">Bind</button>
    <h2 class="underline" >Underlined text</h2>
    <h2 :class="status" class="underline">Status</h2>
    <h2 class="danger" :class="isSafe && 'success' " >Safe</h2>
    <h2 :class="isSafe?'success':'danger'" > {{ isSafe?'success':'danger' }}</h2>
    <h2 :class="['underline','success']" >New</h2>
    <p :class="[ isBig && 'big',isSafe?'success':'danger']" >Conditional Array</p>
    <h2 :class="{
      big:isBig,
      success:isSafe,
      'danger':!isSafe
    }" >COMPLEX</h2>
    <h2 :style="{
      color:highlightColor,
      fontSize:headerSize+'rem',
      padding:'10px'
    }" >Inline Style</h2>
    <h2 :style="headerStyleObject" >Object Styling</h2>
    <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
  </div >
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      greet:'Yo',
      name:"Batman",
      hack:`<a href="#" onclick="alert('you have been hacked')">getsuga tenshou</a>`,
      headingId:'heading',
      status:"success",
      isDisabled:false,
      isSafe:true,
      isBig:false,
      big:'big',
      highlightColor:'orange',
      headerSize:4,
      headerStyleObject:{
        color: 'orange',
        fontSize: '3rem',
        padding: '10px'
      },
      baseStyleObject:{
        fontSize:'50px',
        padding:'10px'
      },
      successStyleObject:{
        color:'green',
        backgroundColor:'tomato',
        border:'3px dashed green',
        fontSize:'70px'
      },
      dangerStyleObject:{
        color:'red',
        backgroundColor:'#4a4ae6',
        border:'4px solid darkred'
      }
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline{
  text-decoration: underline red dashed;
}
.danger{
  color: #d64141;
}
.success{
  color: #28cc5f;
}
.big{
  font-style: italic;
  font-size: 2.5rem;
}
</style>

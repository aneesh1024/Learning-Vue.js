<template>
  <h2>
    {{ name }}
  </h2>
  <div>
    <button class="btn" @click="changeName('Batman',$event),increment(10)">Change Name</button>
  </div>
  <h2>{{ counter }}</h2>
  <div>
    <button class="btn" @click="increment(1)">Increment by 1</button>
    &nbsp;
    <button class="btn" @click="decrement(1)">Decrement by 1</button>
    &nbsp;
    <button class="btn" @click="increment(5)">Increment by 5</button>
    &nbsp;
    <button class="btn" @click="decrement(5)">Decrement by 5</button>
  </div>
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      name:'Aneesh',
      counter:0
    }
  },
  methods:{
    increment(num){
      this.counter += num;
    },
    decrement(num){
      this.counter -= num;
    },
    changeName(newName,event){
      this.name = newName;
      console.log(event)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eee;
  margin-top: 60px;
  background: #2c3e50;
}
body{
  background: #222;

}
.btn{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-size: 1.1rem;
  padding: 5px 10px;
  border-radius: 10px;
  border: none;
  outline: none;
  transition: 0.4s;
  font-weight: 600;
  cursor: pointer;
  border: 4px transparent solid;
}
.btn:active{
  scale: 0.95;
}
.btn:hover{
  border: #d83d29 4px solid;
}
</style>

<template>
  <div>
    <pre>
      {{ formValues }}
    </pre>
  </div>
  <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name">
    </div>
    <div>
      <label for="profileSummary">Profile</label>
      <textarea id="profileSummary" v-model="formValues.profielSummary" />
    </div>
    <div>
      <label for="country">Country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="India">India</option>
        <option value="Japan">Japan</option>
        <option value="USA">USA</option>
        <option value="Russia">Russia</option>
      </select>
    </div>
    <div>
      <label for="jobLocation">Job location</label>
      <select name="jobLocation" multiple id="jobLocation" v-model="formValues.jobLocation">
        <option value="India">India</option>
        <option value="Japan">Japan</option>
        <option value="USA">USA</option>
        <option value="Russia">Russia</option>
        <option value="Vietnam">Vietnam</option>
        <option value="China">China</option>
        <option value="Brazil">Brazil</option>
        <option value="Nepal">Nepal</option>
        <option value="Singapore">Singapore</option>
      </select>
    </div>
    <div>
      <input type="checkbox" name="remoteWork" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
      <label for="remoteWork">Open for remote work ? </label>
    </div>
    <div>
      <label for="skillSet">Skill set  </label>
      <input type="checkbox" id="html" value="HTML" v-model="formValues.skillSet">
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="CSS" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <input type="checkbox" id="js" value="JS" v-model="formValues.skillSet">
      <label for="js">JS</label>
      <input type="checkbox" id="react" value="React" v-model="formValues.skillSet">
      <label for="react">React</label>
      <input type="checkbox" id="vue" value="Vue" v-model="formValues.skillSet">
      <label for="vue">Vue</label>
      <input type="checkbox" id="nodejs" value="Node.js" v-model="formValues.skillSet">
      <label for="nodejs">Node.js</label>
    </div>
    <div>
      <label for="skillSet">Experience</label>
        <input type="radio" id="0-2" value="0-2" v-model="formValues.expreience">
        <label for="0-2">0-2</label>
        <input type="radio" id="3-5" value="3-5" v-model="formValues.expreience">
        <label for="3-5">3-5</label>
        <input type="radio" id="6-10" value="6-10" v-model="formValues.expreience">
        <label for="6-10">6-10</label>
        <input type="radio" id="10+" value="10+" v-model="formValues.expreience">
        <label for="10+">10+</label>
    </div>
    <div>
      <button class="btn" >Submit</button>
    </div>
  </form>
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      name:'Aneesh',
      counter:0,
      formValues:{
        name:'',
        profielSummary:'',
        country:'',
        jobLocation: [],
        remoteWork:"no",
        skillSet:[],
        expreience:''
      }
    }
  },
  methods:{
    submitForm(event){
      event.preventDefault();
      console.log('Form Values',this.formValues);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #eee;
  margin: 5rem;
  margin-top: 60px;
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

form{
  background: #2c3e50;
  width: max-content;
}
form > div{
  border: 1px solid white;
  padding: 10px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
form label{
  margin: 1rem 10px;
}


form input, form textarea{
  margin: 1rem 10px;
  outline: none;
  border: none;
  border-bottom: 1px solid white;
  background: transparent;
  color: white;
  font-size: 1rem;
}
form select{
  padding: 5px 10px;
  font-size: 1rem;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  outline: none;
}

</style>

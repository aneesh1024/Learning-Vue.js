<template>
  <h2>{{ 2+3+10 }}</h2>
  <h2>{{ sum(10,20,30) }}</h2>
  <h2>{{ product(30) }}</h2>
  <h2>{{ mulitply(11) }}</h2>
  <h2>{{ mulitply(pi).toPrecision(4) }}</h2>
  <h2>{{ writeHello(1000) }}</h2>
  <button v-on:click="btnClicked()">Click Me</button>
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      baseMutliplyer:5,
      pi:3.14,
    }
  },
  methods:{
    sum(a,b,c){
      return a+b+c
    },
    product(a = 1,b = 1,c = 1){
      return a*b*c
    },
    mulitply(num){
      return num * this.baseMutliplyer
    },
    writeHello: (num) => {
      return "Hello"+num
    },
    btnClicked(){
      console.log('button clicked')
      alert("Hello")
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
.movie{
  color: tomato;
}
</style>

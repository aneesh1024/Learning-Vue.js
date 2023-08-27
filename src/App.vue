<template>
    <h2 v-if="num === 0">Number is zero</h2>
    <h2 v-else-if="num > 0">Number is greater than 0</h2>
    <h2 v-else-if="num < 0">Number is less than zero</h2>
    <h2 v-else>Not a Number</h2>

    <template v-if="display">
      <h2>Aneesh</h2>
      <h2>Techfluencers</h2>
      <h2>Vue</h2>
    </template>

    <h2 v-show="show">Using v-show</h2>
    <h2 v-if="show">Using v-show</h2>
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      num:'hello',
      display:false,
      show:false,
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

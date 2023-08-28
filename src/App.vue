<template>
   <h2 v-for="(profile, index) in profiles" :key="profile">
    <div>{{ index+1 }}</div>
      <div>{{ profile.name }}</div>
      <div>{{ profile.id }}</div>
   </h2>
   <div v-for="actor in actors" :key="actor">
      <h2>{{ actor.name }}</h2>
      <h3 class="movie" v-for="movie in actor.movies" :key="movie">
        {{ movie }}
      </h3>
   </div>
   <h2 v-for="(value, key, index) in myInfo" :key="value">
    {{ index }}.) {{ key.charAt(0).toUpperCase() + key.slice(1) }} : {{ value }}</h2>
    <template v-for="name in names" :key="name" >
      <h4>
        {{ name }}
      </h4>
      <hr>
    </template>
    <template v-for="n in numbers" :key="n">
      <span v-if="n > 50">{{ n }} &nbsp;</span>
    </template>
</template>
<script>

export default {
  name: 'App',
  data() {
    return {
      names:['Goku','Ichigo','Naruto','Luffy','Natsu','Asta','Deku','Yuji',"Tanjiro"],
      numbers: [10,20,34,11,33,49,40,80,60,89,63],
      profiles: [{
        name: 'Tony',
        id:'1a223b'
      }, {
        name: 'Steve',
        id: '1be33a'
      }, {
        name: 'Ray',
        id: '2a4cc9'
      }],
      actors:[
        {
          name: 'Christian Bale',
          movies: ['Batman','The Prestige']
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic','Inception']
        }
      ],
      myInfo:{
        name:'Aneesh',
        course:'Computer Science',
        id:'303a10222c1052a'
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

<template>
  <div id="app">
    <img alt="itune logo" src="./assets/giphy.gif"  height="250px" width="250px">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    
    <Music /> 
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
//  import Anime from './components/Anime.vue'
import Music from './components/Music.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    Music,
  }
}
</script>

<style>
#app {
  background-image: url(https://cdn.discordapp.com/attachments/746380296630567085/759007680982941696/c1cf6d575178d84528811aa80a5783fa.jpg);
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: 120% ;
  height: 100vh;
  text-align: center;
  font-family: 'Philosopher', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>

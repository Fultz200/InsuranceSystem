<template>
  <img alt="Vue logo" src="./assets/Logo.jpg" class = "img">
  <HelloWorld msg="Welcome"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #060f01;
  margin-top: 20px;
}

.img {
    width: 240px;
    height: 80px;
    margin-bottom: 20px;
}

.controlgood {
  position: absolute;
  left: 4.5%;
  top: 10%;
}

.good {
  position: relative;
}
</style>

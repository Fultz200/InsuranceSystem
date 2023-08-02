<template>
  <div>
    <img alt="Vue logo" src="./assets/Logo.jpg" class = "img">
    <hr />
    <div>
      <!-- <testItem></testItem> -->
      <FiveLipei></FiveLipei>
    </div>
  </div>
</template>

<script>
import FiveLipei from './components/FiveLipei.vue';
// import testItem from './components/testItem.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // TwoZhifu,
    FiveLipei,
    // testItem
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

<!--分割线-->
.tableTitle {
    position: relative;
    margin: 0 auto;
    width: 600px;
    height: 1px;
    background-color: #000000;
    text-align: center;
    font-size: 16px;
    color: rgb(0, 0, 0);
  }
 .midText {
    position: absolute;
    left: 50%;
    background-color: #ffffff;
    padding: 0 15px;
    transform: translateX(-50%) translateY(-50%);
  }
</style>

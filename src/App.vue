<template>
  <div>
    <hr><img alt="Vue logo" src="./assets/Logo.jpg" class = "img">
    <div class="titleText">电子保函测试系统</div><hr>
    <div>
      <!-- <testItem></testItem> -->
      <OneToubao></OneToubao>
    </div>
    <div>
      <FiveLipei></FiveLipei>
    </div>
  </div>
</template>

<script>
import OneToubao from './components/OneToubao.vue';
import FiveLipei from './components/FiveLipei.vue';
// import testItem from './components/testItem.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // TwoZhifu,
    OneToubao,
    FiveLipei,
    // testItem
  }
}
</script>

<style>
.titleText {
  color: rgb(10, 7, 7);
  font-size: 50px;
  line-height: 90px;
  text-align: center;
  width: 50%;
  height: 100%;
  float: right;
}


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

/* <!--分割线--> */
/* hr {
  border: none;
  height: 2px;
  background-color: #333;
  color: #333;
  text-align: center;
} */
/* .hr:after {
  content: "";
  font-size: 20px;
} */
</style>

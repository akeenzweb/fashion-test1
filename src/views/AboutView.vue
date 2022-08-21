<template>
  <div class="about">
    <HeaderNav></HeaderNav>
    <!--<h1>This is an about page</h1>-->
    <div class="container">
      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title1</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title2</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlkhajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknkhajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknk</p>
      </div>
      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title3</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>
      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title4</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknkhajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title5</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title6</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title7</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title8</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>

      <div class="box">
        <img src="../assets/gallary/gal1.jpeg">
        <h2>card title9</h2>
        <p>hajhkjahjkhajh<br>dlahlkhwlkHFWLKj<br>knslvlsnvsnflvslvns<br>jklnvsjnlsbslknknlk</p>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
//import { Stack, StackItem } from 'vue-stack-grid';
import HeaderNav from '../components/header.vue'
export default {
  name: 'HomeView',
  components: {
    //HelloWorld
    //Stack,
    //StackItem
    HeaderNav
  }
}
</script>

<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  width: 500px;
  margin: 0px auto;
  border: 1px solid green;

  columns: 2;
  column-gap: 10px;
}

.box {
  width: 235px;
  padding: 20px;
  background-color: rgb(230, 230, 230);
  border: 1px solid gray;
  /*float: left;
  margin: 10px;*/
  margin-bottom: 10px;
  break-inside: avoid;
}
.box img  {
  width: 100%;
  height: 170px;
  object-fit: contain;
}

.box p {
  width: 50px;
}



</style>
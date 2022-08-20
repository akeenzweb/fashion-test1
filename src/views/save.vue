<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-4"></div>




        <div class="col-md-4 mobile">
          <form>
            <input type="text" placeholder="Search " class="search">
            <!--<i class="fa fa-search" aria-hidden="true"></i>-->
          </form>

          <h2 class="find-your"><b>Find your</b> match style!</h2>

          <div class="row">
            <ul class="category">
              <li class="active-btn">Trends</li>
              <li>2021 New</li>
              <li>Trends</li>
              <li>2021 New</li>
              <li>Trends</li>
              <li>2021 New</li>
              <li>Trends</li>
              <li>2021 New</li>
              <li>Trends</li>
              <li>2021 New</li>

            </ul>
          </div>

          <div class="row" >
            <ul class="gallary masonry-with-columns-2" id="masonry-with-columns-2">
              <li><img src="../assets/gallary/gal1.jpeg"></li>
              <li><img src="../assets/gallary/gal2ii.jpeg"></li>
              <li><img src="../assets/gallary/gal3.jpeg"></li>
              <li><img src="../assets/gallary/gal4.jpeg"></li>
              <!--<li><img src="../assets/gallary/gal5.jpeg"></li>
              <li><img src="../assets/gallary/gal6.jpeg"></li>-->

              <!--<li>rrd</li>
              <li>fxcxc</li>-->
            </ul>
          </div>





        </div>






        <div class="col-md-4"></div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
//import { Stack, StackItem } from "vue-stack-grid";

import Masonry from "masonry-layout"

export default {
  name: 'HomeView',
  components: {
    //HelloWorld

  },
  mounted() {
    // initialize masonry
    var row = document.querySelector("[data-masonry]");
    new Masonry(row, {
      // options
      percentPosition: true,
    });
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Poppins:wght@300;500;600&display=swap');
@import url('http://fonts.cdnfonts.com/css/euclid-circular-a');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  /*font-family: 'Euclid Circular A';*/
  font-family: 'poppins';
}

.mobile {
  border: 1px solid grey;
  height: 100%;
  margin-top: 0px;
  padding: 20px;

  position: relative;
}
.search {
  border: none;
  background: rgb(250, 250, 250);
  width: 100%;
  margin-top: 10px;
  height: 40px;
  border-radius: 10px;
  padding: 10px;
  transition: all ease 0.4s;

  box-shadow: 0 2px 5px rgb(0 0 0 / 0.1);
  /*box-shadow: 0 0 15px #ccc;*/
}
.search:focus {
  transform: scale(1.01);
  padding-left: 15px;
  outline: none;
  border: 1px solid rgb(245, 212, 27);
  transition: all ease 0.4s;
}
.find-your {
  font-family: 'Euclid Circular A';
  width: 190px;
  margin-top: 30px;
  margin-bottom: 40px;
}
.category {
  overflow-x: auto;
  /*position: absolute;*/
  display: flex;
}
/*.category::-webkit-scrollbar {
  width: 0;
}*/
.category li {
  list-style: none;
  /*display: inline-block;*/
  min-width: 120px;
  border: 1px solid rgb(231, 231, 231);
  text-align: center;

  padding-top: 5px;
  padding-bottom: 5px;
  margin-right: 5px;
  border-radius: 10px;
}
.active-btn {
  background: #000;
  color: #fff;
}

.gallary {
  column-count: 1;
}
.gallary li {
  display: inline-block;
  list-style: none;
  width: 47%;
  /*height: 200px;*/
  /*border: 1px solid rgb(182, 183, 243);*/
  margin-top: 10px;
  margin-bottom: 20px;
  border-radius: 16px;
  overflow: hidden;
  column-gap:15px;
}
.gallary li:nth-child(2n){
  /*margin-left: 5px;*/
  float: right;
}
.gallary li img {
  height: 100%;
  width: 100%;
}



/*.masonry-with-flex {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -webkit-flex-direction: column;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-flex-wrap: wrap;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    max-height: 1000px;
  }*/

  /*.masonry-with-flex li {
    width: auto;
    background: #975a58;
    color: white;
    margin: 0 1rem 1rem 0;
    text-align: center;
    font-weight: 900;
    font-size: 2rem;
  }*/



@media screen and (max-width: 425px) {
  .category::-webkit-scrollbar {
    width: 0;
  }
}

</style>

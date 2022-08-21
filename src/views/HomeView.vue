<template>
  <div class="home">
    <headerNav></headerNav>
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <div class="container-fluid">

      <div class="row">
        <div class="col-md-4"></div>




        <div class="col-md-4 mobile">
    <!--<MobileConsole></MobileConsole>-->
          <div class="msg">
            <div v-show="elementVisible" class="msg-wishlist">Added to your Wish list</div>
          </div>
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

              <router-link class="router-link" to="/item"><div v-for="(image, index) in images" :key="index" class="wrap" @click="viewItem(index)"><li ><img :src="image.url"></li><i :class="wishlist ? 'z-index' : 'no-index'" class="fa fa-heart" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><i class="fa fa-heart-o" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><iframe v-show="elementVisible" src="https://embed.lottiefiles.com/animation/91069"></iframe></div></router-link>

              <!--<div class="wrap"><li><img src="../assets/gallary/gal1.jpeg"></li><i :class="wishlist ? 'z-index' : 'no-index'" class="fa fa-heart" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><i class="fa fa-heart-o" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><iframe v-show="elementVisible" src="https://embed.lottiefiles.com/animation/91069"></iframe></div>
              <div class="wrap"><li><img src="../assets/gallary/gal2ii.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal3.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal4.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal5.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal6.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal8.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal9.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal10.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>
              <div class="wrap"><li><img src="../assets/gallary/gal11.jpeg"></li><i class="fa fa-heart" aria-hidden="true"></i><i class="fa fa-heart-o" aria-hidden="true"></i></div>-->


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
//import mobileConsole  from '../components/mobile-console'
import headerNav from "@/components/header.vue";

export default {
  name: 'HomeView',
  components: {
    //HelloWorld
    //mobileConsole,
    headerNav
  },
  data() {
    return {
      wishlist: false,
      elementVisible: false,
      images: [
        {
          url: require('../assets/gallary/gal1.jpeg'),
          name: 'Name 1'
        },
        {
          url: require('../assets/gallary/gal2ii.jpeg'),
          name: 'Name 2'
        },
        {
          url: require('../assets/gallary/gal3.jpeg'),
          name: 'Name 3'
        },
        {
          url: require('../assets/gallary/gal4.jpeg'),
          name: 'Name 4'
        },
        {
          url: require('../assets/gallary/gal5.jpeg'),
          name: 'Name 5'
        },
        {
          url: require('../assets/gallary/gal6.jpeg'),
          name: 'Name 6'
        },
        {
          url: require('../assets/gallary/gal8.jpeg'),
          name: 'Name 8'
        },
        {
          url: require('../assets/gallary/gal9.jpeg'),
          name: 'Name 9'
        },
        {
          url: require('../assets/gallary/gal10.jpeg'),
          name: 'Name 10'
        },
        {
          url: require('../assets/gallary/gal11.jpeg'),
          name: 'Name 11'
        },
      ],
    }
  },
  methods: {
    visible() {
      setTimeout(() => this.elementVisible = false, 2000)
    },
    viewItem(index) {
       this.$store.state.items = this.images[index]
    }
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
  /*border: 1px solid grey;*/
  height: 100%;
  margin-top: 0px;
  padding: 20px;
  padding-bottom: 0%;

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

  padding-top: 8px;
  padding-bottom: 8px;
  margin-right: 5px;
  border-radius: 10px;
}
.active-btn {
  background: #000;
  color: #fff;
}

.gallary {
  /*column-count: 1;*/
  columns: 2;
  column-gap: 10px;
  width: 100%;

  margin-bottom: 60px;
}
.gallary li {
  display: inline-block;
  list-style: none;
  width: 100%;
  /*height: 200px;*/
  /*border: 1px solid rgb(182, 183, 243);*/
  margin-top: 10px;
  margin-bottom: 20px;
  border-radius: 16px;
  overflow: hidden;
  column-gap:15px;
}
.wrap {
  position: relative;
}
.wrap i {
  position: absolute;
  top: 10%;
  right: 10%;
  background-color: #fff;
  padding: 10px;
  border-radius: 50%;
}
.fa-heart {
  color: red;
  /* This z-indez below is when the use clicks the wishlist */
  /*z-index: 1;*/
}
.wrap iframe {
  position: absolute;
  z-index: 1;
  left: 0%;
}
.gallary li:nth-child(2n){
  /*margin-left: 5px;*/
  float: right;
}
.gallary li img {
  height: 100%;
  width: 100%;
  /*z-index: 2;*/
}
.msg-wishlist {
  width: 100%;
  background-color: rgb(68, 219, 131);
  color: #fff;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 20px;
  position: fixed;
  top: 0%;
  opacity: 0.7;
  margin-left: -20px;
  z-index: 1;
  transition: all 0.5s ease;
}
.z-index {
  z-index: 1;
  transition: all 0.5s ease;
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

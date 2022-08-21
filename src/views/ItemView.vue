<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-6 item">
                <!--<img src="../assets/gallary/gal3.jpeg">-->
                <img :src="items.url">
                <router-link to="/" class="router-link"><button><i class="fa fa-arrow-left" aria-hidden="true"></i></button></router-link>
                <i :class="wishlist ? 'z-index' : 'no-index'" class="fa fa-heart" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><i class="fa fa-heart-o" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><iframe v-show="elementVisible" src="https://embed.lottiefiles.com/animation/91069"></iframe>
            </div>
            <div class="col-md-6"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ItemView',
    data() {
    return {
      wishlist: false,
      elementVisible: false,
      images: [
        //{url: require('../assets/gallary/gal1.jpeg') },
        //{url: require('../assets/gallary/gal2ii.jpeg')},
        //{url: require('../assets/gallary/gal3.jpeg')},
        //{url: require('../assets/gallary/gal4.jpeg')},
        //{url: require('../assets/gallary/gal5.jpeg')},
        //{url: require('../assets/gallary/gal6.jpeg')},
        //{url: require('../assets/gallary/gal8.jpeg')},
        //{url: require('../assets/gallary/gal9.jpeg')},
        //{url: require('../assets/gallary/gal10.jpeg')},
        //{url: require('../assets/gallary/gal11.jpeg')},
      ],
      items: {}
    }
  },
  methods: {
    visible() {
      setTimeout(() => this.elementVisible = false, 2000)
    }
  },
  mounted() {
    this.items = this.$store.state.items
    //alert(this.$store.state.count)
  }
}
</script>

<style scoped>

* {
    margin: 0%;
    padding: 0%;
}

li {
    list-style: none;
}
.item {
    position: relative;
}
.item img {
    height: 100%;
    width: 100%;
}
.item i {
  position: absolute;
  top: 5%;
  right: 10%;
  background-color: #fff;
  padding: 10px;
  border-radius: 50%;
}
.item button i {
    right: 88%;
}
.item iframe {
  position: absolute;
  z-index: 1;
  left: 0%;
  top: 0%;
}
.fa-heart {
  color: red;
  /* This z-indez below is when the use clicks the wishlist */
  /*z-index: 1;*/
}
.z-index {
  z-index: 1;
  transition: all 0.5s ease;
}
</style>
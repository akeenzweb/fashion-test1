<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-6 item " id="myId" ref="myId">
                <div class="item-image">
                    <!--<img src="../assets/gallary/gal3.jpeg">-->
                    <img :src="items.url" @dblclick="wishlist = !wishlist; elementVisible = !elementVisible; visible()">
                    <router-link to="/" class="router-link"><button @click="back()"><i class="fa fa-arrow-left" aria-hidden="true"></i></button></router-link>
                    <i :class="wishlist ? 'z-index' : 'no-index'" class="fa fa-heart" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i><i class="fa fa-heart-o" aria-hidden="true" @click="wishlist = !wishlist; elementVisible = !elementVisible; visible()"></i>
                    <!--<iframe v-show="elementVisible" src="https://embed.lottiefiles.com/animation/91069"></iframe>-->
                    <iframe v-show="elementVisible" class="love-animation love-icon-scale" src="https://embed.lottiefiles.com/animation/53105"></iframe>
                    <iframe v-show="elementVisible" class="love-animation love-icon-scale" src="https://embed.lottiefiles.com/animation/101775"></iframe>
                    <iframe v-show="elementVisible" class="love-animation" src="https://embed.lottiefiles.com/animation/35288"></iframe>
                </div>
                <div class="swipe">
                    <i class="fa fa-angle-double-down" aria-hidden="true"></i>
                    <p>Swipe down for details</p>
                </div>

                <div class="slide">
                    <ul >
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                        <li><img src="../assets/gallary/gal1.jpeg"></li>
                    </ul>
                </div>
            </div>
            <div class="col-md-6 details-column">
                <div class="details">
                    <p>Men's Category</p>
                    <h2>Jean Jacket</h2>
                    <h2><b>$5000</b></h2>
                </div>

                <div class="quantity">
                    <button class="count-btn">
                        <span @click="minus()">-</span> {{count}} <span @click="add()">+</span>
                    </button>

                    <p>Description</p>
                    <h4>buweudcdfuwhuhbu8y u28u2hdf82hedf 2hdf82u 82hedf82 f238fd8 23df</h4>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
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
      count: 1,
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
    },
    minus() {
        if (this.count>= 2){
            this.count--
        }

    },
    add() {
        this.count++
    }
    //back() {
    //    this.$store.state.items = {}
    //}
  },
  mounted() {
    this.items = this.$store.state.items
    //alert(this.$store.state.count)
  }
//  created() {
//    this.$refs.myId.scrollIntoView()
//  }
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
.item-image i {
  position: absolute;
  top: 5%;
  right: 5%;
  background-color: #fff;
  padding: 10px;
  border-radius: 50%;
}

.item button i {
    right: 88%;
}
.item .love-anime {
  position: absolute;
  z-index: 1;
  left: 0%;

  /* New styles */
  top: 30%;
  transform: scale(1.9);
  /*transition: all 0.4s ease;*/
}
.love-animation {
    position: absolute;
    z-index: 1;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.love-icon-scale {
    /*scale: 2;*/
    height: 300px;
    width: 300px;
}
.fa-heart {
  color: red;
  /* This z-indez below is when the use clicks the wishlist */
  /*z-index: 1;*/
}
.fa-heart-o {
    color: #000;
}
.z-index {
  z-index: 1;
  transition: all 0.5s ease;
}

.slide {
    background: rgb(245, 245, 245);
    padding: 4px;
    width: fit-content;
    position: absolute;
    right: 5%;
    top: 25%;
    text-align: center;
    border-radius: 10px;

}
.slide ul {
    max-height: 300px;
    overflow: scroll;
}
.slide li {
    width: 50px;
    overflow: hidden;
    list-style: none;
}
.slide li img {
    width: 100%;
    height: 100%;
    border-radius: 10px;
    margin: 2px;
}
.swipe {
    position: absolute;
    bottom: 5%;
    text-align: center;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgb(245, 245, 245);
}
.swipe i {
    top: 5%;
    right: 5%;
    background-color: none;
    padding: 0px;
    border-radius: 100%;
    animation: pointer 1s infinite;
}
.row {
    background-color: #000;
    color:#fff;
}
@keyframes pointer {
    20% {transform: translateY(5px);};
    40% {transform: translateY(0px);};
    60% {transform: translateY(10px);};
    80% {transform: translateY(5px);};
    100% {transform: translateY(0px);};
}
.details-column {
    /*background-color: #000;
    color:#fff;*/
    /*width: 100vw;
    height: 100vh;*/
    /*height: 100vh;*/
    padding: 20px;
}
.details {
    position: relative;
}
.details p {
    color: rgb(248, 248, 248);
    font-style: italic;
}
.details h2 {
    display: inline-block;
}
.details h2:nth-child(3) {
    float: right;
    /*color: aqua;*/
}
.quantity span {
    padding: 20px;
}
.count-btn {
    /*display: inline;*/
    margin-top: 20px;
    border: 1px solid #fff;
    text-align: center;
    color: #fff;
    background-color: #000;
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 10px;
}
.quantity p {
    color: rgb(248, 248, 248);
    font-style: italic;
    margin-top: 30px;
}
.add-to-cart {
    padding: 10px;
    margin-top: 20px;
    padding-left: 20px;
    padding-right: 20px;
    border-radius: 10px;
}
</style>
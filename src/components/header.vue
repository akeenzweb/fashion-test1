<template>
    <div id="nav-background">
        <nav class="navbar navbar-expand-lg bg-white py-3">
  <div class="container-fluid">
    <a class="navbar-brand" href="#"><h1><b>KUZA</b></h1></a>
    <div @click="showMenu = !showMenu" class="navbar-toggler " type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </div>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link to="/" exact>Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" exact>About us</router-link>
        </li>

        <li class="nav-item">
          <router-link to="/policy" exact>Shipping</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/policy" exact>Sign in</router-link>
        </li>

      </ul>

    </div>
  </div>
</nav>
    </div>
</template>

<script>

export default {
  name: 'AboutView',
  data() {
    return {
        showMenu: false
    }
  }
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500&family=Poppins:wght@300;500;600&display=swap');
@import url('http://fonts.cdnfonts.com/css/euclid-circular-a');
* {
    margin: 0%;
    padding: 0%;
    font-family: 'poppins';
}

@keyframes bounce {
    from {transform: translateY(-10px);};
    to {transform: translateY(0px);}
}

ul {
    transform: translateX(50px);
}

nav {
    /*margin: 15px;*/
    transform: translateY(15px);
    margin-left: 81px;
    margin-right: 81px;
    border-radius: 50px;
}
.navbar {
    /*border: 1px solid red;*/
    padding: 60px 30px 60px 30px;
    height: 70px;


    /*background: linear-gradient(90deg, rgba(242,180,159,1) 0%, rgba(232,168,166,1) 35%, rgba(254,223,166,1) 60%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    border: 2px solid white;*/
}
nav img {
    height: 50px;
    width: 150px;
}
li {
    font-size: 16px;
    line-height: 22px;
    margin-left: 15px;
    margin-right: 15px;
    font-family: Inter;
    font-weight: 400;
    padding-top: 10px;


}
li:hover {
    transform: translateY(-5px);
    transition: all 0.4s ease;
}
li:nth-child(1) {
    animation-name: bounce;
    animation-duration: 1.5s;
    transition: all 0.4s ease;
}
li:nth-child(2) {
    animation-name: bounce;
    animation-duration: 1.5s;
    animation-delay: 0.5s;
    transition: all 0.4s ease;
}
li:nth-child(3) {
    animation-name: bounce;
    animation-duration: 1.5s;
    animation-delay: 1s;
    transition: all 0.4s ease;
}
li:nth-child(4) {
    animation-name: bounce;
    animation-duration: 1.5s;
    animation-delay: 1.5s;
    transition: all 0.7s ease-in-out;
}


a {
    color: black;
    text-decoration: none;
    font-size: 18px;
    line-height: 22px;
}
a:hover {
    color: #D392C5;

}
.download-button {
    padding: 18px 46px 18px 39px;
    /*width: 230px;
    height: 62px;*/
    border-radius: 40px;
    font-family: 'Inter';
    font-style: normal;
    color: #fff;
    background-color: black;
    padding-left: -2px;
    text-align: center;
}
button img {
    width: 32px;
    height: 20px;
    padding: 2px;
    transform: translateX(20px);
}
.navbar-toggler  {
    /*color: rgb(255, 255, 255);*/
    margin-right: -20px;
}
/*.navbar-toggler span {
    color: rgb(2, 0, 0);
    width: 22px;
    height: 2px;
}*/
#nav-background {
    /*background: #a728a7;*/
    margin: 0%;
    padding: 0%;
    top: 0%;
    /*position: fixed;
    width: 100vw;*/

}
.menu-bar {
    width: 100%;
    height: 100%;
}
.router-link {
    text-decoration: none;

}

.router-link-active {
  background: #fff;
  color: #b92828;
  padding: 5px;
  border-radius: 5px;
}
.input-group-text {
    background: black;
    color: #fff;
}


@media screen and (max-width: 700px){
    ul {
        text-align: left;
        transform: translateX(0px);
    }
    nav {
        margin: 0;
        transform: translateY(0px);
        border-radius: 0%;
    }
    nav img {
        height: 40px;
        width: 130px;
    }
    li {
        margin-left: 0%;
        margin-right: 0%;
        margin-top: 15px;
    }

    button img {
        width: 32px;
        height: 20px;
    }
    .download-button {
        margin: 10px 0px 10px 0px;
    }
    .navbar {
        height: unset;
    }
}
</style>
<template>
    <nav class="navbar is-transparent">
        <div class="nav-overlay" @click="showNav = !showNav" :class="{ 'is-active': showNav }"></div>
        <div class="navbar-brand">
            <div class="navbar-item">
                <nuxt-link :to="'/'">
                    <div class="is-uppercase logo" :class="{'has-text-white': hero}"><strong>Max</strong>López</div>
                </nuxt-link>
            </div>
        <!--
    Using the v-on: directive to listen for the click event and toggle the data property showNav. Also, using the v-bind: directive to reactively update the class attribute 'is-active' based on the showNav property.
    -->
        <div class="navbar-burger" @click="showNav = !showNav" :class="{ 'is-active': showNav }">
          <span :style="{color: 'hsl(210, 86%, 39%)'}" :class="{'has-text-white': hero}"></span>
          <span :style="{color: 'hsl(210, 86%, 39%)'}" :class="{'has-text-white': hero}"></span>
          <span :style="{color: 'hsl(210, 86%, 39%)'}" :class="{'has-text-white': hero}"></span>
        </div>
      </div>
      <!--
    Using the v-bind: directive to reactively update the class attribute 'is-active' based on the showNav property.
    -->
      <div class="navbar-menu" :class="{ 'is-active': showNav }">
        <div class="navbar-end">
            <ul class="navbar-item">
                <nuxt-link :to="'/'">
                    <li class="cool-link" :class="{'has-text-blue': home}">
                      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="is-hidden-desktop">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
                      </svg>
                      Home
                    </li>
                </nuxt-link>
                <nuxt-link :to="'/about-me'" class="about" >
                    <li class="cool-link" :class="{'has-text-blue': home}">
                      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="is-hidden-desktop">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.121 17.804A13.937 13.937 0 0112 16c2.5 0 4.847.655 6.879 1.804M15 10a3 3 0 11-6 0 3 3 0 016 0zm6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                      </svg>
                      About me
                    </li>
                </nuxt-link>
            </ul>
        </div>
      </div>
    </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['hero', 'home'],
  data () {
    return {
      showNav: false
    }
  },
  head() {
    return{
      script: [
        {
          src:'https://use.fontawesome.com/releases/v5.3.1/js/all.js'
        }
      ]
    }
  }
}
</script>

<style scoped>
    body{
        margin: 0;
    }
    .navbar{
      margin-top: 18px;
      z-index: 99;
    }
    li {
        list-style: none;
        color: hsl(210, 75%, 25%);
        margin-right: 32px;
        font-size: 16px;
        letter-spacing: 0.15em;
        font-weight: normal;
    } 
    
    .nuxt-link-exact-active li{
      border-bottom: 2px solid #3173B4;
    }
    .nuxt-link-exact-active.is-white li{
      border-bottom: 2px solid white;
    }
    .nuxt-link-exact-active li:hover{
      border-bottom: none;
    }
    .logo{
        font-family: 'Nunito', sans-serif;
        font-size: 24px;
        color: hsl(210, 75%, 25%);
    }
    .navbar-menu{
        font-family: 'Nunito', sans-serif;
        font-weight: 600;
    }
    .button{
        font-family: 'Nunito', sans-serif;
        font-size: 16px;
        border-radius: 8px;
        background: white;
        color: #24A2D0;
        border: none;
        padding: 18px;
        display: flex;
        align-items: center;
    }
    .cool-link{
      color: white;
    }
    .cool-link::after{
      content:'';
      display:block;
      width: 0;
      height: 2px;
      background: white;
      transition: width .3s;
      border-radius: 1px;
    }
    .has-text-white::after{
      content:'';
      display:block;
      width: 0;
      height: 2px;
      background: white;
      transition: width .3s;
      border-radius: 1px;
    }
    .has-text-white:hover:after{
      width: 100%;
      transition: width .3s;
    }
    .cool-link:hover:after{
      width: 100%;
      transition: width .3s;
    }
    svg{
      width: 18px;
      margin-right: 8px;
    }
    .about{
      pointer-events: none;
    }
    .has-text-blue{
      color: #3173B4
    }
    @media screen and (max-width: 1023px) {
      .navbar{
        margin-top: 0;
      }
      .navbar-brand .navbar-item{
        padding-left: 0;
      }
      .navbar-burger{
        z-index: 3;
        right: -24px;
      }
      .navbar-burger.is-active{
        position: fixed;
        top: 0;
        right: 0;
      }
      .navbar-menu{
        position: fixed;
        top: 0;
        right: 0;
        height: 100vh;
        width: 80%;
        box-shadow: 0 0 0 8px rgba(0, 0, 0, 0.1);
      }
    
      ul{
        padding: 48px 24px;
        height: 100vh;
        z-index: 2;
      }
      ul .button{
        font-size: 20px;
      }
      li{
        display: flex;
        align-items: center;
        margin-bottom: 24px;
        margin-right: 0px;
        font-size: 20px;
        color: hsl(212, 45%, 58%);
      }
      svg{
        width: 24px;
        height: 24px;
        margin-right: 8px;
      }
      .button{
        width: 100%;
        animation: none;
      }
      .nuxt-link-exact-active li{
        color: hsl(210, 86%, 39%);
        border-bottom: none;
      }
      .nav-overlay{
        position: fixed;
        top: 0;
        left: 0;
        width: 20%;
        height: 100vh;
        background: rgba(0, 0, 0, 0.3);
        backdrop-filter: blur(2px);
        visibility: hidden;
        opacity: 0;
        z-index: 1;
      }
      .nav-overlay.is-active{
        visibility: visible;
        opacity: 1;
      }
      .cool-link{
        color: #3173B4;
      }
      .cool-link:hover:after{
        width: 0;
        transition: 0;
      }
  }
</style>
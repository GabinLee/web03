<template>
  <div id="app">
    <header>
      <div class="h-container mw1440">
        <div class="logo-box">
          <router-link to="/" class=" logo-font">Sample</router-link>
        </div>

        <nav class="nav-box uppercase fs16">
          <router-link to="/" @click.native="clickNavItem(1)" :class="{ checked: selectedIndex == 1 ? true : false}">
            <span>home</span>
          </router-link>
          <router-link to="/about" @click.native="clickNavItem(2)" :class="{ checked: selectedIndex == 2 ? true : false}">
            <span>about</span>
          </router-link>
          <router-link to="/product" @click.native="clickNavItem(3)" :class="{ checked: selectedIndex == 3 ? true : false}">
            <span>product</span>
          </router-link>
          <router-link to="/contact" @click.native="clickNavItem(4)" :class="{ checked: selectedIndex == 4 ? true : false}">
            <span>contact</span>
          </router-link>
        </nav>

        <div class="mobile-menu-btn">
          <button v-ripple @click="openMobileNav">
            <v-icon>mdi-menu</v-icon>
          </button>
        </div>        
      </div>
    </header>

    <div id="mobile-nav-container" @click="closeMobileNav">
      <div id="mobile-nav-box" class="fs16 uppercase">
        <button v-ripple @click="closeMobileNav">
          <v-icon>mdi-close</v-icon>
        </button>
        <router-link to="/" @click.native="clickNavItem(1)" :class="{ checked: selectedIndex == 1 ? true : false}" v-ripple>
          <p>home</p>
        </router-link>
        <router-link to="/about" @click.native="clickNavItem(2)" :class="{ checked: selectedIndex == 2 ? true : false}" v-ripple>
          <p>about</p>
        </router-link>
        <router-link to="/product" @click.native="clickNavItem(3)" :class="{ checked: selectedIndex == 3 ? true : false}" v-ripple>
          <p>product</p>
        </router-link>
        <router-link to="/contact" @click.native="clickNavItem(4)" :class="{ checked: selectedIndex == 4 ? true : false}" v-ripple>
          <p>contact</p>
        </router-link>
      </div>
    </div>
    
    <main>
      <div class="m-container mw1440">
        <router-view/>
      </div>
    </main>

    <footer>
      <div class="f-container mw1440">
        <div class="group">
          <div class="info-box">
            <p class="j-title uppercase">call</p>
            <p class="j-text">000-0000-0000</p>
          </div>
          <div class="info-box">
            <p class="j-title uppercase">e-mail</p>
            <p class="j-text">sample@gmail.com</p>
          </div>
          <div class="info-box">
            <p class="j-title uppercase">address</p>
            <p class="j-text">Gyeonggi</p>
          </div>
          <div class="info-box">
            <p class="j-title uppercase">find me</p>
            <p class="j-text">instagram</p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>


<script>
export default {
  data: () => ({
    selectedIndex : 1
  }),
  methods: {
    clickNavItem(index) {
      this.selectedIndex = index
    },
    openMobileNav() {
      document.getElementById('mobile-nav-container').style.width = "100%"
      document.getElementById('mobile-nav-box').style.width = "300px"
    },
    closeMobileNav() {
      document.getElementById('mobile-nav-container').style.width = "0"
      document.getElementById('mobile-nav-box').style.width = "0"
    }
  }  
}
</script>


<style lang="scss">
/* default setting */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto Mono', monospace;
 }
  html, body{ font-size: 10px; }
  a{ display: inline-block; text-decoration: none; color: inherit; }
  button{ background-color: transparent; border: none; cursor: pointer; }
  button:focus{ outline: none; }
  img{ display: inline-block; width: 100%; margin-bottom: 30px; }

  .mw1440{ max-width: 1440px; margin: 0 auto; padding-left: 40px; padding-right: 40px; }
  .fs16{ font-size: 16px; }

  .j-top-head{ font-size: 50px; margin-bottom: 40px; }
  .j-head{ font-size: 32px; margin-bottom: 24px; }
  .j-title{ font-size: 20px; margin-bottom: 16px; }
  .j-text{ font-size: 16px; }

  .logo-font{ font-family: 'Delius Swash Caps', cursive; }
  .padding-50{ padding: 50px; }
  .padding-tb-50{ padding-top: 50px; padding-bottom: 50px; }
  .padding-lr-50{ padding-left: 50px; padding-right: 50px; }
  .padding-20{ padding: 20px; }
  .uppercase{ text-transform: uppercase; }
  .bg-gray{
    width: 100%;
    height: 100%;
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
    letter-spacing: 10px;
  }



  #app{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
/* header */
  header{
    height: 80px;
    .logo-box{
      padding: 10px 0;
      a{
        height: 100%;
        color: #1BB850;
        display: flex;
        align-items: center;
        font-size: 40px;
      }
    }
    .nav-box{
      margin-right: -20px;
      a{
        height: 100%;
        line-height: 80px;
        margin-right: 20px;
        padding: 0 20px;
      }
      a:last-child{
        margin-right: 0;
      }
      a:hover{
        transition: all 0.2s ease;
      }
      span{
        position: relative;
        letter-spacing: 1px;
      }
      span:before{
        content: "";
        height: 3px;
        border-left: 12px solid #1BB850;
        border-right: 12px solid #1BB850;
        opacity: 0;
        position: absolute;
        top: 50%;
        left: 20%;
        right: 20%;
        transform: translateY(-50%);
        transition: all 0.35s ease;
      }
      a:hover span:before, .checked span:before{
        opacity: 1;
        left: -16px;
        right: -16px;
      }
    }
  }
  .h-container{
    height: 100%;
    display: flex;
    justify-content: space-between;
  }

  .mobile-menu-btn{
    margin-right: -10px;
    display: none;
    button{
      color: #1bb850;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      margin: 10px 0;
    }
    button:hover{
      background-color: rgba(27, 182, 79, .2);
    }
  }
  #mobile-nav-container{
    background-color: rgba(0, 0, 0, .8);
    width: 0;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    z-index: 999;
    cursor: pointer;
  }
  #mobile-nav-box{
    background-color: #fff;
    width: 0;
    height: 100%;
    margin-left: auto;
    display: flex;
    flex-direction: column;
    transition: .5s;
    overflow: hidden;
    
    button{
      color: #1bb850;
      width: 40px;
      height: 40px;
      margin: 10px 30px 10px auto;
      border-radius: 50%;
    }
    button:hover{
      background-color: rgba(27, 182, 79, .2);
    }
    a{
      color: #1bb850;
      margin: 10px;
      border-radius: 5px;
      padding: 14px 0;
      text-align: center;
      p{
        color: #000;
      }
    }
    a:hover{ background-color: rgba(27, 182, 79, .2); }
  }


/* main */
  main{ overflow: hidden; }


/* footer */
  footer{
    background-color: #bebebe;
    margin-top: auto;
    .group{
      margin: 0 -20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .info-box{
      width: 25%;
      padding: 30px 20px;
      text-align: center;
    }
  }



/* 반응형 */
@media (max-width: 1080px) {
}

@media (max-width: 900px) {
  footer{
    .info-box{
      width: 50%;
      padding: 20px;
    }
  }
}

@media (max-width: 768px) {
  .j-top-head{ font-size: 40px; margin-bottom: 30px; }
  .j-head{ font-size: 28px; margin-bottom: 20px; }
  img{ margin-bottom: 20px; }
  .bg-gray{ font-size: 60px; }
  
  header{
    .nav-box{
      display: none;
    }
  }
  .mobile-menu-btn{
    display: block;
  }
}

@media (max-width: 600px) {
  .mw1440{ padding-left: 20px; padding-right: 20px; }
  .j-top-head{ font-size: 36px; margin-bottom: 26px; }
  .j-head{ font-size: 24px; margin-bottom: 16px; }
  .j-title{ font-size: 16px; margin-bottom: 10px; }
  .j-text{ font-size: 12px; }
  img{ margin-bottom: 10px; }
  .bg-gray{ font-size: 40px; }

  header{
    height: 60px;
    .logo-box{
      a{
        font-size: 30px;
      }
    }
  }
}

</style>

<template>
  <nav class="navbar is-transparent is-fixed-top" :class="{'scroll-active': scroll}" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a role="button" class="navbar-burger has-text-white" aria-label="menu" aria-expanded="false" @click="toggleMenu">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div class="navbar-menu">
      <div class="container">
        <div class="navbar-end">
          <a class="navbar-item has-text-white ancla" href="#sect1">Page 1</a>
          <a class="navbar-item has-text-white ancla" href="#sect2">Page 2</a>
          <a class="navbar-item has-text-white ancla" href="#sect3">Page 3</a>
          <div class="navbar-item">
            <div class="buttons">
              <a class="button ancla" href="#header">
                Top
              </a>
              <a class="button has-text-white" @click="scrollNext">
                bottom
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  data () {
    return {
      scroll: false
    }
  },
  methods: {
    toggleMenu (e) {
      const $target = document.querySelector('.navbar-menu')
      const $navbarBurger = document.querySelector('.navbar-burger')
      $navbarBurger.classList.toggle('is-active')
      $target.classList.toggle('is-active')
    },
    scrollNext () {
      let valScroll = document.documentElement.scrollTop
      const heightHeader = window.$('#header').height()
      const heightSect1 = window.$('#sect1').height()
      const heightSect2 = window.$('#sect2').height()
      const heightSect3 = window.$('#sect3').height()
      if (valScroll < heightHeader) {
        window.$('html, body').animate({ scrollTop: (window.$('#sect1').position().top) }, 1000)
        return
      }
      if (valScroll >= heightHeader && valScroll <= (heightHeader + heightSect1 - 1)) {
        window.$('html, body').animate({ scrollTop: (window.$('#sect2').position().top) }, 1000)
        console.log('entro2')
        return
      }
      if (valScroll >= heightHeader + heightSect1 && valScroll <= heightHeader + heightSect1 + heightSect2 - 1) {
        window.$('html, body').animate({ scrollTop: (window.$('#sect3').position().top) }, 1000)
        return
      }
      if (valScroll >= heightHeader + heightSect1 + heightSect2 - 2 && valScroll <= heightHeader + heightSect1 + heightSect2 + heightSect3 - 1) {
        window.$('html, body').animate({ scrollTop: (window.$('#sect4').position().top) }, 1000)
      }
    }
  },
  mounted () {
    let self = this
    window.$(window).scroll(() => {
      if (window.$(window).scrollTop() > 60) {
        self.scroll = true
      } else {
        self.scroll = false
      }
    })
  }
}
</script>
<style lang="scss">
  @media only screen and (min-width: 1088px) {
    .navbar .navbar-menu .container {
      padding: 3rem 0;
    }
  }
  @media only screen and (max-width: 1088px) {
    .navbar {
      background-color: rgba(0, 0, 0, .4) !important;
      .navbar-menu{
        background-color: rgba(0, 0, 0, .4) !important;
      }
    }
    .scroll-active{
    background-color: rgba(0, 0, 0, .4)!important;
    .navbar-menu .container{
      padding: 0 !important;
    }
  }
    a.navbar-item:hover{
      background-color: transparent !important;
    }
  }
  .navbar .navbar-menu .navbar-item .buttons .button{
    width: 9rem;
  }
  .navbar .navbar-menu .navbar-item .buttons .button:nth-of-type(2){
    background-color: transparent !important;
    color: white;
  }
  .navbar .navbar-menu a.navbar-item{
    padding: 0 1.5rem;
  }
  .scroll-active{
    background-color: rgba(0, 0, 0, .4)!important;
    .navbar-menu .container{
      padding: 1rem 0;
    }
  }
</style>

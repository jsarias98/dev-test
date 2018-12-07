<template>
    <header class="hero is-fullheight-with-navbar is-medium has-carousel" id="header">
      <div class="hero-head">
        <nav-bar/>
      </div>
      <carousel/>
      <div class="columns is-mobile">
        <div class="column is-two-fifths-mobile is-two-fifths-tablet is-one-fifth-desktop is-one-fifth-widescreen">
          <div class="buttons">
            <a class="button is-medium is-fullwidth has-text-white ancla" href="#sect1">Go to Bottom</a>
          </div>
        </div>
      </div>
    </header>
</template>
<script>
import NavBar from './nav'
import Carousel from './carousel'
export default {
  components: {
    NavBar,
    Carousel
  }
}
</script>
<style lang="scss">
.columns.is-mobile .column{
  margin: auto;
  .buttons .button{
    background-color: #501086;
    border: solid #501086;
    font-weight:700;
    font-size: 1em;
    margin-bottom: 3em;
    box-shadow: 0 2px 2px 0 rgba(0,0,0,0.14), 0 3px 1px -2px rgba(0,0,0,0.12), 0 1px 5px 0 rgba(0,0,0,0.2);
  }
}
.hero.is-fullheight-with-navbar {
  height: 100vh !important;
}

</style>

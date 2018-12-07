<template>
  <div class='hero-carousel carousel-animated carousel-animate-slide'>
    <div class='carousel-container' >
      <div class='carousel-item has-background is-active' v-for="(item, index) in slider" :key="index">
        <img class="is-background" :src="item.image" alt="" width="640" height="310" />
        <div class="hero-body">
          <div class="container">
            <h1 class="title has-text-white">
              <strong>{{item.title.split(' ')[0]}}</strong>
              {{item.title.split(' ')[1]}}
            </h1>
            <h2 class="subtitle has-text-grey-lighter">
              {{item.text}}
            </h2>
          </div>
        </div>
      </div>
    </div>
    <div class="carousel-navigation is-overlay">
      <div class="column carousel-nav-left transparent">
        <font-awesome-icon icon="caret-left" />
      </div>
      <div class="column carousel-nav-right">
        <font-awesome-icon icon="caret-right" />
      </div>
    </div>
  </div>
</template>
<script>
import bulmaCarousel from 'bulma-carousel'
export default {
  data () {
    return {
      slider: []
    }
  },
  mounted () {

  },
  async created () {
    await this.getDataSlider()
  },
  methods: {
    async getDataSlider () {
      try {
        this.slider = await fetch('https://api.myjson.com/bins/17ocpi').then(res => res.json())
      } catch (er) {
        throw new Error(er)
      }
      bulmaCarousel.attach()
    }
  }
}
</script>
<style lang="scss">
.carousel-item .hero-body{
  position: absolute;
  width: 70%;
  height: fit-content;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  h1{
    position: relative !important;
    background-color: transparent !important;
    font-size: 3.8em !important;
    padding: .9em 0 !important;
    font-weight: 600;
    strong {
      font-weight: 300;
    }
  }
  h2{
    position: relative !important;
    text-align: center;
    color: gray ;
    font-size: 1em !important;
    line-height: 2em;
  }
}
.carousel-nav-left,
.carousel-nav-right {
  background-color: transparent !important;
  border-radius: 50%;
  border: solid 2px white;
  width: 2.7em !important;
  height: 2.7em !important;
  color: white !important;
}
.carousel-nav-left{
  margin-left: 8.33333%;

}
.carousel-nav-right{
  margin-right: 8.33333%;
}
@media screen and (max-width: 769px) {
  .carousel-nav-left{
    margin-left: 3%;

  }
  .carousel-nav-right{
    margin-right: 3%;
  }
  .carousel-item .hero-body {
    width: 85%;
    h1{
      font-size: 2em !important;
    }
  }
}
</style>

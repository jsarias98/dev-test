<template>
  <section class="hero is-fullheight section4" id="sect4">
    <div class="hero-body">
      <div class="container">
        <h1 class="has-text-white">THANK <strong class="has-text-white">YOU</strong></h1>
      </div>
    </div>
    <div class="columns is-mobile">
      <div class="column is-two-fifths-mobile is-two-fifths-tablet is-one-fifth-desktop is-one-fifth-widescreen">
        <div class="buttons">
          <a class="button is-medium is-fullwidth has-text-white ancla" href="#header">Go to Header</a>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {

}
</script>
<style lang="scss">
.hero.section4{
    background-color: #5c109c;
    .columns{
      margin-bottom: 0 ;
    }
  }
  .hero.section4 .hero-body .container {
    width: 80%;
    max-width: 80%;

    .card .card-content .content{
      text-align: center;
    }
    h1{
      text-align: center;
      font-size: 2.8em;
    }
  }
  @media screen and (max-width: 769px) {
    .hero.section4 .hero-body .container h1{
      font-size: 2em;
      margin-bottom: 3rem;
    }
  }
</style>

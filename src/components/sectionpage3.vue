<template>
  <section class="hero is-fullheight section3" id="sect3">
    <div class="hero-body">
      <div class="container">
        <h1 class="has-text-white">PAGE 3 <strong class="has-text-white">JUST IMAGES</strong></h1>
        <div class="columns">
          <div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="../assets/card-1.png" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="content has-text-grey-light">SO NICE</div>
              </div>
            </div>
          </div>
          <div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="../assets/card-2.png" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="content has-text-grey-light">SO COOL</div>
              </div>
            </div>
          </div>
          <div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="../assets/card-3.png" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="content has-text-grey-light">SO PEACEFUL</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-mobile">
      <div class="column is-two-fifths-mobile is-two-fifths-tablet is-one-fifth-desktop is-one-fifth-widescreen">
        <div class="buttons">
          <a class="button is-medium is-fullwidth has-text-white ancla" href="#sect4">Go to Bottom</a>
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
  .hero.section3{
    background-color: #420e6f;
  }
  .hero.section3 .hero-body .container {
    width: 80%;
    max-width: 80%;
    .card .card-content .content{
      text-align: center;
    }
    h1{
      text-align: center;
      margin-bottom: 4.5rem;
      font-size: 2.8em;
    }
  }
  @media screen and (max-width: 769px) {
    .hero.section3 .hero-body .container h1{
      font-size: 2em;
      margin-bottom: 3rem;
    }
  }
</style>

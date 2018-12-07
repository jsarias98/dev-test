<template>
  <section class="hero is-fullheight section2" id="sect2">
    <div class="hero-body">
      <div class="container">
        <h1 class="has-text-white">PAGE 2 <strong class="has-text-white">TEXT</strong></h1>
        <div class="columns">
          <div class="column is-full-mobile">
            <p class="has-text-white">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias qui illo veniam nisi explicabo illum dignissimos facilis? Adipisci itaque in ad sequi quasi. Porro rerum, odit, vel, nobis quidem exercitationem enim nesciunt eveniet iure perspiciatis dicta quam quisquam facere. Necessitatibus.</p>
            <p class="has-text-white">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt, a eaque magni laudantium laboriosam, ipsa facilis magnam, vero recusandae animi qui nisi minima fuga quibusdam! Nemo, eius impedit ullam tempora, in accusantium maiores dolor adipisci ad debitis consequuntur quo dicta!</p>
          </div>
          <div class="column is-full-mobile">
            <p class="has-text-white">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias qui illo veniam nisi explicabo illum dignissimos facilis? Adipisci itaque in ad sequi quasi. Porro rerum, odit, vel, nobis quidem exercitationem enim nesciunt eveniet iure perspiciatis dicta quam quisquam facere. Necessitatibus.</p>
            <p class="has-text-white">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt, a eaque magni laudantium laboriosam, ipsa facilis magnam, vero recusandae animi qui nisi minima fuga quibusdam! Nemo, eius impedit ullam tempora, in accusantium maiores dolor adipisci ad debitis consequuntur quo dicta!</p>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-mobile">
      <div class="column is-two-fifths-mobile is-two-fifths-tablet is-one-fifth-desktop is-one-fifth-widescreen">
        <div class="buttons">
          <a class="button is-medium is-fullwidth has-text-white ancla" href="#sect3">Go to Bottom</a>
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
  .hero.section2{
    background-color: #501086;
  }
  .hero.section2 .hero-body .container {
    width: 80%;
    max-width: 80%;
    .column{
      text-align: justify;
      p:nth-of-type(2){
        margin-top: 2em;
      }
    }
    h1{
      text-align: center;
      margin-bottom: 4.5rem;
      font-size: 2.8em;
    }
  }
  @media screen and (max-width: 769px) {
    .hero.section2 .hero-body .container h1{
      font-size: 2em;
      margin-bottom: 3rem;
    }
  }

</style>

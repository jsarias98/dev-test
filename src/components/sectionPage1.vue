<template>
  <section class="hero is-fullheight section1" id="sect1">
    <div class="hero-body">
      <div class="container">
        <h1 class="has-text-white">PAGE 1 <strong class="has-text-white">CHECK FIELDS</strong></h1>
        <div class="columns ">
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 1...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question1" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 2...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question2" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 3...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question3" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="columns ">
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 4...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question4" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 5...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question5" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-full-mobile">
            <div class="columns is-mobile">
              <div class="column question has-text-white is-half-mobile">
                <span>QUESTION 6...</span>
              </div>
              <div class="column is-half-mobile">
                <div class="select is-fullwidth">
                  <select v-model="question6" @change="validationQuestion">
                    <option value="yes">YES</option>
                    <option value="no">NO</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="columns">
          <div class="column">
            <p class="has-text-white" v-for="(item, index) in questionChange" :key="index">Question change: .... {{item}}</p>
          </div>
        </div>
        <div class="columns">
          <div class="column">
            <p class="has-text-grey-light" >* if any answer on the form is "Yes" then the console must show a "true" message</p>
            <p class="has-text-grey-light">* if all answer on the form is "No" then the console must show a "false" message</p>
          </div>
        </div>
      </div>
    </div>
    <div class="columns is-mobile">
      <div class="column is-two-fifths-mobile is-two-fifths-tablet is-one-fifth-desktop is-one-fifth-widescreen">
        <div class="buttons">
          <a class="button is-medium is-fullwidth has-text-white ancla" href="#sect2">Go to Bottom</a>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      question1: 'yes',
      question2: 'yes',
      question3: 'yes',
      question4: 'yes',
      question5: 'yes',
      question6: 'yes',
      questionChange: []
    }
  },
  methods: {
    validationQuestion () {
      let heightConsole = window.$('.hero.section1 .hero-body .container>.columns:nth-of-type(3)>.column')[0].scrollHeight
      if (this.question1 === 'yes' || this.question2 === 'yes' || this.question3 === 'yes' || this.question4 === 'yes' || this.question5 === 'yes' || this.question6 === 'yes') {
        this.questionChange.push(true)
        window.$('.hero.section1 .hero-body .container>.columns:nth-of-type(3)>.column').animate({ scrollTop: heightConsole }, 1000)
      } else if (this.question1 === 'no' && this.question2 === 'no' && this.question3 === 'no' && this.question4 === 'no' && this.question5 === 'no' && this.question6 === 'no') {
        this.questionChange.push(false)
        window.$('.hero.section1 .hero-body .container>.columns:nth-of-type(3)>.column').animate({ scrollTop: heightConsole }, 1000)
      }
    }
  }
}
</script>
<style lang="scss">
  .hero.section1{
    background-color: #5c109c;
  }
  .hero.section1 .hero-body .container {
    width: 80%;
    max-width: 80%;
    .question {
      font-weight: 700;
      display: flex;
      text-align: center;
      align-items: center;
      justify-content: center;
    }
    &>.columns:nth-of-type(2){
      margin-top: 1.5em;
    }
    &>.columns:nth-of-type(3){
      margin-top: 1em;
      background-color: #531788;
      padding: .3em 1em;
      .column {
        overflow-y: scroll;
        height: 72px;
      }
    }
    h1{
      text-align: center;
      margin-bottom: 4.5rem;
      font-size: 2.8em;
    }
  }
  @media screen and (max-width: 769px) {
    .hero.section1 .hero-body .container h1{
      font-size: 2em;
      margin-bottom: 3rem;
    }
  }
</style>

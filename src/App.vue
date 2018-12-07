<template>
  <div id="app">
    <header-sigma/>
    <section1 />
    <section2 />
    <section3 />
    <section4 />
  </div>
</template>

<script>
import HeaderSigma from './components/header'
import Section1 from './components/sectionPage1'
import Section2 from './components/sectionPage2'
import Section3 from './components/sectionpage3'
import Section4 from './components/sectionPage4'

export default {
  name: 'app',
  components: {
    HeaderSigma,
    Section1,
    Section2,
    Section3,
    Section4
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>

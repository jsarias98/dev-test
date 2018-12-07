<template>
  <div id="app">
    <header-sigma/>
    <section1 />
  </div>
</template>

<script>
import HeaderSigma from './components/header'
import Section1 from './components/sectionPage1'

export default {
  name: 'app',
  components: {
    HeaderSigma,
    Section1
  }
}
</script>

<style lang="scss">
@import './scss/main.scss'
</style>

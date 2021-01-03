<template>
  <div id="app">
    <navbar />
    <hero />
    <about />
    <!-- <investors /> -->
    <partner />
    <footer-element />
  </div>
</template>

<script>
import Partner from './components/Partner'
import FooterElement from './components/footer'
import Navbar from './components/navbar'
import Hero from './components/hero'
import About from './components/About'
// import Investors from './components/Investors'

export default {
  name: 'App',
  components: {
    FooterElement,
    Partner,
    Navbar,
    Hero,
    About,
    // Investors,
  }
}
</script>

<style lang="scss" src="./scss/reset.scss"></style>

<style>
  #app {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background: #F8F9FB;
  }
</style>

<template>
  <div id="app">
    <navigation />
    <hero />
    <services />
    <vision />
    <investors />
    <partner />
    <footer-element />
  </div>
</template>

<script>
import Vue from 'vue';
import Partner from './components/Partner'
import FooterElement from './components/footer'
import Hero from './components/hero'
import Services from './components/Services'
import Investors from './components/Investors'
import Vision from './components/vision.vue'
import Navigation from '@/components/Global/Nav';

Vue.component('navigation', Navigation);

export default {
  name: 'App',
  components: {
    FooterElement,
    Partner,
    Hero,
    Services,
    Investors,
    Vision,
  }
}
</script>

<style lang="scss" src="./scss/reset.scss"></style>

<style>
  #app {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /* background: #FDFDFE; */
    background-image: linear-gradient(0deg, #FDFDFE, #f5f7fa);
  }
</style>

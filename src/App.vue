<template>
  <div id="app" class="app">
    <navigation />
    <div class="container">
      <home />
      <products />
      <why-spaces />
      <people />
      <partner />
      <el-footer />
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import VueSmoothScroll from 'vue2-smooth-scroll'
import Navigation from '@/components/Global/Navigation/Nav';
import Home from '@/Pages/Home';
import Products from '@/Pages/Products';
import WhySpaces from '@/Pages/WhySpaces';
import People from '@/Pages/People';
import Partner from '@/Pages/Partner';
import ElFooter from '@/components/ElFooter';

Vue.use(VueSmoothScroll);

export default {
  name: 'App',
  components: {
    Navigation,
    Home,
    Products,
    WhySpaces,
    People,
    Partner,
    ElFooter,
  }
};
</script>

<style src="./assets/css/reset.css"></style>
<style src="./assets/css/variables.css"></style>
<style src="./assets/css/main.css"></style>

<style>
@media screen and (min-width: 768px) {
  .container {
    max-width: 144rem;
    margin: 0 auto;
  }
}

</style>

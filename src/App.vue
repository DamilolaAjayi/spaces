<template>
  <div id="app" class="app">
    <navigation />
    <div class="container">
      <home :openModal="openModal" @modal-is-open="modalIsOpen" @merchant-count="merchantCount"/>
      <products :openModal="openModal" @modal-is-open="modalIsOpen" />
      <why-spaces :openModal="openModal" @modal-is-open="modalIsOpen" />
      <people :openModal="openModal" @modal-is-open="modalIsOpen" />
      <partner :openModal="openModal" @modal-is-open="modalIsOpen" :merchant_count="merchant_count" />
      <el-footer :openModal="openModal" @modal-is-open="modalIsOpen" />
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
  },
  data() {
    return {
      openModal: false,
      merchant_count: 110000,
    };
  },
  methods: {
    modalIsOpen(value) {
      this.openModal = value;
    },
    merchantCount(payload) {
      this.merchant_count = payload;
    },
  },
};
</script>

<style src="./assets/css/reset.css"></style>
<style src="./assets/css/variables.css"></style>
<style src="./assets/css/main.css"></style>

<style>
.modal-is-open {
  -webkit-filter: blur(8px);
  filter: blur(8px);
  opacity: 1;
}
.el-dialog {
  max-width: 90%;
}
@media screen and (min-width: 768px) {
  .container {
    max-width: 144rem;
    margin: 0 auto;
  }
}

</style>

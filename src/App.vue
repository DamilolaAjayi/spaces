<template>
  <div id="app" class="app">
    <navigation />
    <div class="container">
      <home />
      <products />
      <why-spaces />
      <team />
      <partner />
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/Global/Navigation/Nav';
import Home from '@/Pages/Home';
import Products from '@/Pages/Products';
import WhySpaces from '@/Pages/WhySpaces';
import Team from '@/Pages/Team';
import Partner from '@/Pages/Partner';

export default {
  name: 'App',
  components: {
    Navigation,
    Home,
    Products,
    WhySpaces,
    Team,
    Partner,
  }
};
</script>

<style src="./assets/css/reset.css"></style>
<style src="./assets/css/variables.css"></style>
<style src="./assets/css/main.css"></style>

<style>
.container {
  max-width: 90%;
  margin: 0 auto;
}
@media screen and (min-width: 768px) {
  .container {
    max-width: 120rem;
    margin: 0 auto;
  }
}

</style>

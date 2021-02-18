<template>
  <div id="app" class="app">
    <navigation />
    <div class="container">
      <home />
      <team />
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/Global/Navigation/Nav';
import Home from '@/Pages/Home';
import Team from '@/Pages/Team';

export default {
  name: 'App',
  components: {
    Navigation,
    Home,
    Team,
  }
};
</script>

<style src="./assets/css/reset.css"></style>
<style src="./assets/css/variables.css"></style>
<style src="./assets/css/main.css"></style>

<style>
.container {
  max-width: 120rem;
  margin: 0 auto;
}
</style>

<template>
  <div class="nav-mobile">
    <ul class="nav-mobile-list">
      <li><a href="#products" class="nav-link" @click="hideNavBody">Products</a></li>
      <li>
        <a href="#purpose" class="nav-link" @click="hideNavBody">Purpose</a>
      </li>
      <li>
        <a href="#team" class="nav-link" @click="hideNavBody">Team</a>
      </li>
      <li>
        <a href="#partner" class="nav-link" @click="hideNavBody">Partner</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'mobile-nav',
  methods: {
    hideNavBody() {
      this.$emit("menuClicked");
    },
  },
};
</script>

<style scoped>
.nav-mobile {
  position: absolute;
  top: 4.8rem;
  font-size: 1.2em;
  left: 0px;
  width: 100%;
  height: 100vh;
  margin: 0px;
}
.nav-mobile-list {
  text-align: center;
  line-height: 2.5em;
  width: 100%;
}
.nav-mobile-list:first-child {
  margin-top: 2em;
}
</style>

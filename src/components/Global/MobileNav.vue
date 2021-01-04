<template>
  <div class="nav-mobile">
    <ul class="nav-mobile-list">
      <li><a href="#about" class="nav-link" @click="hideNavBody">About</a></li>
      <li><a href="#partner" class="nav-link" @click="hideNavBody">Partner</a></li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'mobile-nav',
  methods: {
      hideNavBody() {
          this.$emit('menuClicked');
      },
  },
};
</script>

<style lang="scss" scoped>
  .nav-mobile {
    position: absolute;
    top: 4rem;
    font-size: 1.2em;
    left: 0px;
    width: 100%;
    height: 100vh;
    margin: 0px;
    background: white;
    .nav-mobile-list {
      text-align: center;
      line-height: 5em;
      background: white;
      width: 100%;
      :first-child{
        margin-top: 2em;
      }
    }
  }
</style>

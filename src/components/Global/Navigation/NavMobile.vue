<template>
  <div>
    <div class="nav__dropdown">
      <button class="nav-dropdown__btn">
        <div class="nav-dropdown__avatar"></div>
      </button>
      <div class="nav-dropdown__list">
        <a href="#products" class="nav-link" @click="hideNavBody" v-smooth-scroll="{ duration: 1000, offset: -50 }">Products</a>
        <a href="#purpose" class="nav-link" @click="hideNavBody" v-smooth-scroll="{ duration: 1000, offset: -50 }">Purpose</a>
        <a href="#team" class="nav-link" @click="hideNavBody" v-smooth-scroll="{ duration: 1000, offset: -50 }">Team</a>
        <a href="#partner" class="nav-link" @click="hideNavBody" v-smooth-scroll="{ duration: 1000, offset: -50 }">Partner</a>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'nav-mobile',
};
</script>

<style scoped>
.nav__dropdown {
  float: left;
  overflow: hidden;
}
.nav__dropdown .nav-dropdown__btn {
  border: none;
  outline: none;
  background-color: inherit;
  font-family: inherit;
  margin: 0;
}
.nav-dropdown__avatar {
		height: 25px;
		width: 25px;
		background: whitesmoke;
    border-radius: 50%;
    margin: 0;
}
.nav-link {
  float: none;
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  text-align: left;
}
.nav__dropdown:hover .nav-dropdown__list {
  display: block;
}
.nav-dropdown__list {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}
</style>

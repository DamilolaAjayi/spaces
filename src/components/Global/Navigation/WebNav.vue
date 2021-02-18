<template>
  <div class="web-nav">
    <a href="#product" class="web-nav-link">Product</a>
    <a href="#purpose" class="web-nav-link">Purpose</a>
    <a href="#team" class="web-nav-link">Team</a>
    <a href="#partner" class="web-nav-link">Partner</a>
  </div>
</template>

<script>
export default {
  name: "web-nav",
};
</script>

<style scoped>
.web-nav {
  display: flex;
  justify-content: flex-end;
  margin: 0 auto;
}
.web-nav-link {
  padding: 0 2rem;
  position: relative;
  display: inline-block;
  vertical-align: top;
  text-decoration: none;
  text-align: left;
  font-size: 1.6rem;
  line-height: 2.4rem;
  font-weight: 500;
}
</style>

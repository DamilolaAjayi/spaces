<template>
  <div class="nav">
    <div class="nav-mobile" v-if="isMobile">
        <img v-if="!menuClicked" src="@/assets/menu.svg" @click="toggleMenu" alt="Menu Icon">
        <img class="close-button" v-else src="@/assets/close-button.svg" @click="toggleMenu" alt="Close Icon">
        <mobile-nav v-if="showMobileNav" />
    </div>
    <div class="nav-web" v-else>
        <web-nav />
    </div>
  </div>
</template>

<script>
import IsMobile from '@/mixins/IsMobile';
import WebNav from './WebNav';
import MobileNav from './MobileNav';

export default {
  mixins: [IsMobile],
  components: {
    MobileNav,
    WebNav,
  },
  data() {
    return {
      showMobileNav: false,
      menuClicked: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMobileNav = !this.showMobileNav;
      this.menuClicked = !this.menuClicked;
    },
  }
}
</script>

<style lang="scss" scoped>
.nav {
    z-index: 3;
    position: relative;
    &-mobile {
        padding: 1rem 1.5rem;
        display: flex;
        justify-content: flex-end;
        width: 100%;
        position: fixed;
        background: white;
    }
    &-content {
    //   width: inherit;
      @media screen and (max-width: 767px) {
        display: flex;
        justify-content: flex-end;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
      }
    }
  }
</style>

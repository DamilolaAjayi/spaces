<template>
  <main id="home">
    <div class="hero-page section-container">
      <div class="hero-page__textbox">
        <h2>
          Empowering small merchants to grow big profits.
        </h2>
        <p class="hero-page__brief">
          Over 100,000 retailers have put their trust in Spaces to digitize
          their business. Spaces helps you track your sales and customers,
          provide a broader assortment for your clients, facilitate access to
          finance, manage your logistics and grow your business quickly.
        </p>
        <button v-if="!isMobile" class="s-button" @mouseover="animateButton" @mouseleave="removeButtonAnimation">
            <span :class="{'animate-btn-text' : animateButtonChevron}">Download App</span>
            <i class="fas fa-chevron-circle-right" :class="{'chevron-r' : animateButtonChevron}"></i>
        </button>
        <a class="app-link" v-else>
         <span>Download App</span>
          <i class="fas fa-external-link-square-alt"></i>
        </a>
      </div>
      <div class="hero-page__carousel">
          <carousel :mouse-drag="false" :per-page="1" :autoplay="true" :speed="1500" :loop="true" :autoplayDirection="'forward'">
              <slide>
                <img src="http://placehold.it/600x400" alt="" />
              </slide>
              <slide>
                <img src="http://placehold.it/600x400" alt="" />
              </slide>
              <slide>
                <img src="http://placehold.it/600x400" alt="" />
              </slide>
          </carousel>
      </div>
    </div>
  </main>
</template>

<script>
import IsMobile from '@/mixins/IsMobile';
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "Home",
  components: {
    Carousel,
    Slide,
  },
mixins: [IsMobile],
  data() {
    return {
      data: [
        '<img src="http://placehold.it/600x400" alt="" />',
        '<img src="http://placehold.it/600x400" alt="" />',
        '<img src="http://placehold.it/600x400" alt="" />',
      ],
      animateButtonChevron: false,
    };
  },
  methods: {
      animateButton() {
          this.animateButtonChevron = true;
      },
      removeButtonAnimation() {
          this.animateButtonChevron = false;
      },
  },
};
</script>

<style scoped>
.s-button {
    width: 100%;
    max-width: 34.6rem;
    height: 7.4rem;
    font-size: 2.8rem;
    font-weight: 300;
    position: relative;
}
.hero-page__brief {
    padding: 3rem 0;
    font-size: 1.6rem;
}
.s-button span {
    margin-left: -10px;
}
.app-link {
    font-size: 1.8rem;
    color: var(--primaryOne);
}
.app-link:hover {
    color: var(--primaryTwo);
    opacity: 1;
}
.app-link .fas {
    padding-left: 0.5rem;
}
.hero-page {
    display: flex;
    flex-direction: column;
    margin-top: 10rem;
}
.hero-page__textbox {
    color: black;
    margin-bottom: 4rem;
}
.hero-page__carousel {
    max-width: 90%;
    margin: 0 auto;
}
.fa-chevron-circle-right {
    position: absolute;
    top: 32%;
    padding-left: 1rem;
}
.animate-btn-text {
    font-weight: 600;
    transition: font-weight .4s ease-in-out
}
.chevron-r {
    animation-duration: 0.5s;
    animation-fill-mode: forwards;
    animation-iteration-count: 1;
    animation-name: animateButton;
    animation-timing-function: ease;
}
@keyframes animateButton {
    15% {
        right: 50px;
    }
    100% {
        right: 30px;
    }
}
@media screen and (min-width: 768px) {
    .hero-page {
        flex-direction: row;
        justify-content: space-between;
        margin-top: 8rem;
        padding-top: 5rem;
    }
    .hero-page__brief {
        padding: 3rem 0;
        font-size: 1.6rem;
    }
    .hero-page__textbox {
        color: black;
        max-width: 50rem;
        margin-bottom: 4rem;
    }
    .hero-page__carousel {
        max-width: 600px;
        margin: 0;
    }
}
@media screen and (max-width: 767px) {
    main {
        min-height: auto;
    }
}
</style>

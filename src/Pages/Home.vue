<template>
  <main id="home">
    <div class="hero-page">
      <div class="hero-page__textbox">
        <h2>
          Empowering small merchants to grow big profits.
        </h2>
        <p>
          Over 100,000 retailers have put their trust in Spaces to digitize
          their business. Spaces helps you track your sales and customers,
          provide a broader assortment for your clients, facilitate access to
          finance, manage your logistics and grow your business quickly.
        </p>
        <button class="s-button">Download App</button>
      </div>
      <div class="hero-page__carousel">
          <carousel :mouse-drag="false" :per-page="1" :autoplay="true" :speed="1500" :loop="true" :autoplayDirection="'forward'">
              <slide @slideclick="handleSlideClick">
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
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "Home",
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      data: [
        '<img src="http://placehold.it/600x400" alt="" />',
        '<img src="http://placehold.it/600x400" alt="" />',
        '<img src="http://placehold.it/600x400" alt="" />',
      ],
    };
  },
  methods: {
    handleSlideClick (dataset) {
        console.log(dataset.index, dataset.name)
    }
  },
};
</script>

<style scoped>
.s-button {
    width: 28rem;
}
.hero-page {
    display: flex;
    flex-direction: column;
    margin-top: 8rem;
}
.hero-page__carousel {
    max-width: 90%;
    margin: 0 auto;
}
@media screen and (min-width: 768px) {
    .hero-page {
        flex-direction: row;
        justify-content: space-between;
        margin-top: 8rem;
    }
    .hero-page__textbox {
    color: black;
    }
    .hero-page__carousel {
        max-width: 600px;
    }
}

</style>

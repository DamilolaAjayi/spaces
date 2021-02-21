<template>
  <main id="purpose">
    <div class="company section-container">
      <header class="purpose__header">
        <h2>Why Use Spaces</h2>
        <img class="purpose__header-image" src="@/assets/Underline-5-Blue.png" alt="">
      </header>
      <div class="company-purpose">
        <carousel
          :mouse-drag="false"
          :per-page="1"
          :autoplay="true"
          :speed="500"
          :loop="true"
          :autoplayDirection="'forward'"
        >
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Increased Demand</h3>
                <p>
                  Access to our robust e-commerce platform for wholesale and
                  retail.
                </p>
              </div>
              <div>
                <img src="http://placehold.it/600x400" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Improved Cashflow</h3>
                <p>Credit facilities that ensure business needs are met.</p>
              </div>
              <div>
                <img src="http://placehold.it/600x400" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Streamlined logistics</h3>
                <p>
                  Streamlining the flow of goods from distributors and wholesalers
                  to merchants.
                </p>
              </div>
              <div>
                <img src="http://placehold.it/600x400" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Automatic savings</h3>
                <p>
                  Streamlining the flow of goods from distributors and wholesalers
                  to merchants.
                </p>
              </div>
              <div>
                <img src="http://placehold.it/600x400" alt="" />
              </div>
            </div>
          </slide>
        </carousel>
      </div>
    </div>
  </main>
</template>

<script>
/* eslint-disable */
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "why-spaces",
  components: {
    Carousel,
    Slide,
  },
};
</script>

<style scoped>
.section-container {
  background-color: var(--semanticTwo);
  padding-top: 5rem;
  padding-bottom: 5rem;
}
.company {
  text-align: center;
}
.purpose__header {
  width: max-content;
  margin: 0 auto 4rem auto;
  max-width: 100%;
}
.purpose__header-image {
    height: 30px;
    margin-top: -8px;
    width: 100%;
}
.company-purpose__block {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
@media screen and (max-width: 767px) {
    main {
        min-height: auto;
    }
}
</style>

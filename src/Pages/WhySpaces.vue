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
                <!-- <p class="company-purpose__brief">
                  Access to our robust e-commerce platform for wholesale and
                  retail.
                </p> -->
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/demand.jpg" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Improved Cashflow</h3>
                <!-- <p class="company-purpose__brief">Credit facilities that ensure business needs are met.</p> -->
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/cashflow.jpg" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Streamlined logistics</h3>
                <!-- <p class="company-purpose__brief">
                  Streamlining the flow of goods from distributors and wholesalers
                  to merchants.
                </p> -->
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/logistics.jpg" alt="" />
              </div>
            </div>
          </slide>
          <slide>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Automatic savings</h3>
                <!-- <p class="company-purpose__brief">
                  Streamlining the flow of goods from distributors and wholesalers
                  to merchants.
                </p> -->
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/savings.jpg" alt="" />
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
.company-purpose {
  margin: 0 auto;
  max-width: 90%;
}
.company-purpose__block {
  display: flex;
  justify-content: space-between;
  /* align-items: center; */
}
.company-purpose__textbox {
  padding-top: 5rem;
  text-align: left;
  max-width: 40rem;
}
.company-purpose__textbox h3 {
  width: max-content;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--primaryOne);
}
.company-purpose__brief {
  font-size: 2rem;
  font-weight: 400;
}
.company-purpose-block__image {
  width: 600px;
  max-height: 40rem;
}
@media screen and (max-width: 767px) {
    main {
        min-height: auto;
    }
}
</style>

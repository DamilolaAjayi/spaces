<template>
  <main id="purpose">
    <div class="company section-container">
      <header class="purpose__header">
        <h2>Why Use Spaces</h2>
        <img class="purpose__header-image" src="@/assets/Underline-5-Blue.png" alt="">
      </header>
      <div class="company-purpose" v-if="!isMobile">
        <agile
          :autoplay="true"
          :speed="1000"
        >
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Increased
                  <br>Demand</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/demand.jpg" alt="" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Improved 
                 <br>Cashflow</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/cashflow.jpg" alt="" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Streamlined
                  <br>logistics</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/logistics.jpg" alt="" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Automatic
                  <br>savings</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/savings.jpg" alt="" />
              </div>
            </div>
        </agile>
      </div>
      <div v-else>
        <div class="company-purpose__block">
          <div class="company-purpose-block__image">
            <img src="@/assets/images/demand.jpg" alt="" />
          </div>
          <div class="company-purpose__textbox">
            <h3>Increased Demand</h3>
          </div>
        </div>
        <div class="company-purpose__block">
          <div class="company-purpose-block__image">
            <img src="@/assets/images/cashflow.jpg" alt="" />
          </div>
          <div class="company-purpose__textbox">
            <h3>Improved Cashflow</h3>
          </div>
        </div>
        <div class="company-purpose__block">
          <div class="company-purpose-block__image">
            <img src="@/assets/images/logistics.jpg" alt="" />
          </div>
          <div class="company-purpose__textbox">
            <h3>Streamlined logistics</h3>
          </div>
        </div>
        <div class="company-purpose__block">
          <div class="company-purpose-block__image">
            <img src="@/assets/images/savings.jpg" alt="" />
          </div>
          <div class="company-purpose__textbox">
            <h3>Automatic savings</h3>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import IsMobile from "@/mixins/IsMobile";
import { VueAgile } from 'vue-agile'
/* eslint-disable */

export default {
  name: "why-spaces",
  components: {
    agile: VueAgile,
  },
  mixins: [IsMobile],
};
</script>

<style scoped>
    main {
        min-height: auto;
    }
    .purpose__header-image {
        height: 30px;
        margin-top: -8px;
        max-width: 75%;
    }
    .company-purpose__block {
      display: flex;
      width: 100%;
      flex-direction: column;
      justify-content: center;
    }
    .company-purpose__textbox h3 {
      font-weight: 400;
      font-size: 2rem;
    }
    .company-purpose-block__image {
      width: 200px;
      max-height: 20rem;
    }
@media screen and (min-width: 768px) {
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
  flex-direction: row;
}
.company-purpose__textbox {
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  max-width: 40rem;
}
.company-purpose__textbox h3 {
  font-weight: 600;
  font-size: 4rem;
}
.company-purpose__brief {
  font-size: 2rem;
  font-weight: 400;
}
.company-purpose-block__image {
  width: 600px;
  max-height: 40rem;
}
}
</style>

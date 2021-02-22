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
        <div class="group">
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Increase
                  demand</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/demand.jpg" alt="" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Improve 
                 cash flows</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/cashflow.jpg" alt="" />
              </div>
            </div>
        </div>
        <div class="group">
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Streamlined
                  logistics</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/logistics.jpg" alt="" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose__textbox">
                <h3>Automatic
                  savings</h3>
              </div>
              <div class="company-purpose-block__image">
                <img src="@/assets/images/savings.jpg" alt="" />
              </div>
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
            <h3>Increase demand</h3>
          </div>
        </div>
        <div class="company-purpose__block">
          <div class="company-purpose-block__image">
            <img src="@/assets/images/cashflow.jpg" alt="" />
          </div>
          <div class="company-purpose__textbox">
            <h3>Improve cash flows</h3>
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

export default {
  name: "why-spaces",
  components: {
    agile: VueAgile,
  },
  mixins: [IsMobile],
};
</script>

<style scoped>
  .group {
    display: flex;
  }
  .section-container {
    background-color: var(--semanticTwo);
  }
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
      width: 250px;
    }
@media screen and (min-width: 768px) {
  .section-container {
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
  width: 100%;
  position: relative;
}
.company-purpose__textbox {
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
  /* position: absolute;
  top: 20px; */
  color: var(--primaryTwo);
}
.company-purpose__textbox h3 {
  font-weight: 600;
  font-size: 4rem;
  color: var(--primaryFour);
}
.company-purpose__brief {
  font-size: 2rem;
  font-weight: 400;
}
.company-purpose-block__image {
  width: 100%;
  max-height: 35rem;
  height: 35rem;
  border: 5px solid var(--semanticFour);
  overflow: hidden;
}
.company-purpose-block__image {
  /* make top blur for header text*/
  /* background: linear-gradient(#fff, #020202, transparent), url("../assets/images/cashflow.jpg") no-repeat center; */
  /* background-image: linear-gradient(top, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0) 59%, rgba(0, 0, 0, 0.65) 100%)!important; */
}
}
@media screen  and (max-width: 767px) {
  .section-container {
    text-align: center;
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
  .company-purpose__block {
    align-items: center;
    padding: 4rem 0;
  }
  .company-purpose__block__image {
    margin-bottom: 1rem;
  }
}
</style>

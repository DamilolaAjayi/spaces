<template>
  <section class="company-about__section section-container" id="partner">
      <header class="company-about__header">
        <h2>Why partner with us</h2>
          <transition
          mode="in-out"
          enter-active-class="animate__animated animate__flipInX"
          >
          <h3 v-if="runanimation">
          We have an unparalleled understanding of the
          <a
              target="_blank"
              href="https://www.boi.ng/wp-content/uploads/2018/05/BOI-Working-Paper-Series-No2_Economic-Development-through-the-Nigerian-Informal-Sector-A-BOI-perspective.pdf"
          >
              informal sector
          </a>
          </h3>
        </transition>
      </header>
    <div class="company-portfolio">
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/product.svg" alt="">
          <h4>
              You have a product or service you want to provide to 
          <strong>
            <ICountUp
              :delay="delay"
              :endVal="endVal"
              :duration="200"
              :options="options"
              @ready="onReady"
            />
          </strong>
          merchants?
          </h4>
      </div>
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/performance.svg" alt="">
          <h4>
              You want to track performance and preferences for your product or service?
          </h4>
      </div>
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/distribution.svg" alt="">
          <h4>
              Largest informal distribution channel in Africa. 
          </h4>
      </div>
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/merchants.svg" alt="">
          <h4>
              <strong>100,000</strong> active merchants, 
              <strong>10,000</strong> agents across Nigeria, <br>
              <strong>$1.5 billion</strong> in recorded sales
          </h4>
      </div>
    </div>
  </section>
</template>

<script>
import ICountUp from 'vue-countup-v2';
export default {
  components: {
    ICountUp,
  },
  data() {
    return {
      delay: 1500,
      endVal: 100000,
      runanimation: false,
      instance: null,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ',',
        decimal: '.',
        prefix: '',
        suffix: '',
      }
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    onReady(instance) {
      this.instance = instance;
      this.rerunCountUp(instance)
    },
    rerunCountUp(instance) {
      instance.reset();
      instance.start();
      setTimeout(() => {
        this.onReady(instance);
      }, 10000);
    },
  },
};
</script>

<style scoped>
.company-about__header {
    margin-bottom: 2rem;
}
.company-about__header h3 {
    margin: 4rem 0;
    opacity: 0.7;
    font-size: 3rem;
}
.company-about__section {
  text-align: center;
  background: var(--semanticTwo);
}
.company-portfolio__card {
  overflow: hidden;
  padding: 3rem 2rem;
  width: 250px;
  margin: 0 auto;
  z-index: 9;
  background: var(--semanticOne);
  box-shadow: 1px 1px 4px #8C7B7B;
  border-radius: 6px;
  margin-bottom: 2rem;
  background-image: linear-gradient(to top, #c9c8c8 #fafdff);
}
.company-portfolio__card img {
  width: 10rem;
  border-radius: 4px;
  filter: drop-shadow(0 0 0.4rem #c9c8c8);
}
.company-portfolio__card h4 {
  text-align: left;
  margin-top: 2rem;
}
@media screen and (min-width: 768px) {
  .company-about__section {
    padding-top: 5rem;
    padding-bottom: 5rem;
  }
  .company-portfolio {
    display: flex;
    justify-content: space-between;
    margin-top: 6rem;
  }
  .company-portfolio__card {
    overflow: hidden;
    width: 250px;
    z-index: 9;
    background: var(--semanticOne);
    box-shadow: 0px 1px 6px rgb(0 0 0 / 8%);
    border-radius: 6px;
    background-image: linear-gradient(to top, #fafdff, #fff);
  }
}
@media screen and (max-width: 767px) {
  .section-container {
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
}
</style>

<template>
  <section class="company-about__section section-container" id="partner" :class="{'modal-is-open' : openModal}">
      <header class="company-about__header">
        <h3>Why partner with us?</h3>
        <img src="@/assets/Underline-5-Blue.png" alt="">
        <transition
          mode="in-out"
          enter-active-class="animate__animated animate__flipInX"
          >
          <h4 v-if="runanimation" class="subtitle">
           We have an unparalleled understanding of the informal sector
          </h4>
        </transition>
      </header>
    <div class="company-portfolio">
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/product.svg" alt="">
          <p>
              You have a product or service you want to provide to 
          <strong>
            <ICountUp
              :delay="delay"
              :endVal="endVal"
              :duration="300"
              :options="options"
              @ready="onReady"
            />
          </strong>
          merchants.
          </p>
      </div>
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/performance.svg" alt="">
          <p>
              You want to track performance and preferences for your product or service.
          </p>
      </div>
      <div class="company-portfolio__card">
          <img src="@/assets/images/partner/distribution.svg" alt="">
          <p>
              Largest informal distribution channel in Africa with over $1.5b in recorded sales and 10,000 agents across Nigeria.
          </p>
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
  props: {
    openModal: Boolean,
  },
  data() {
    return {
      delay: 1500,
      endVal: 109733,
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
    handleScroll() {
      if (window.pageYOffset > 2000) {
        this.runanimation = true;
      }
    },
  },
};
</script>

<style scoped>
.company-about__header {
    margin-bottom: 3rem;
}
.company-about__header h3 {
    width: max-content;
    margin: 0 auto;
}
  .company-about__header img {
      height: 2.5rem;
      width: 32rem;
      margin-top: -5px;
  }
.company-about__section {
  text-align: center;
  background: var(--semanticTwo);
}
.company-portfolio__card {
  overflow: hidden;
  padding: 3rem 0 2rem;
  width: 25rem;
  margin: 0 auto;
  z-index: 9;
  background: var(--semanticOne);
  box-shadow: 0px 1px 6px rgb(0 0 0 / 8%);
  border-radius: 6px;
  margin-bottom: 2rem;
  background-image: linear-gradient(to top, #E5F4FF, #fff);
}
.subtitle {
  color: var(--primaryTwo);
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
p {
  text-align: left;
  color: var(--primaryOne);
  font-weight: 500;
  padding-bottom: 0;
  margin-top: 1.5rem;
  border-top: 0.2px solid rgba(201, 200, 200, 0.3);
  padding: 1.5rem;
}
@media screen and (min-width: 768px) {
  .company-about__section {
    padding-top: 5rem;
    padding-bottom: 5rem;
  }
  .company-about__header {
      margin-bottom: 2rem;
  }
  .company-about__header img {
      height: 2.5rem;
      width: 32rem;
      margin-top: -5px;
  }
  .company-portfolio {
    display: flex;
    justify-content: space-between;
    margin: 6rem auto 0;
    max-width: 100rem;
  }
}
@media screen and (max-width: 767px) {
  .section-container {
    padding-top: 3rem;
    padding-bottom: 4rem;
  }
  .subtitle {
    font-size: 1.4rem;
  }
  .company-about__header img {
    width: 23rem;
  }
}
</style>

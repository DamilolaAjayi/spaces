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
              <strong>100k</strong> active merchants, 
              <strong>10,000</strong> agents across Nigeria, <br>
              <strong>$1.5 billion</strong> in recorded sales
          </h4>
      </div>
    </div>
    <div class="spaces-contact">
      <a target="_blank" :href="`mailto:info@spaces.io`" class="contact"
        >info@spaces.io</a
      >
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
      delay: 1000,
      endVal: 100000,
      runanimation: false,
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
    checkOffset() {
      console.log(window.pageYOffset);
    },
    onReady: function(instance) {
      const that = this;
      instance.update(that.endVal + 0);
    },
    handleScroll() {
      if (window.pageYOffset > 2299) {
        this.onReady();
      }
      if (window.pageYOffset > 2199) {
        this.runanimation = true;
      }
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
    /* color: var(--primaryOne); */
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
  z-index: 2;
  background: var(--semanticOne);
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
  border-radius: 6px;
  margin-bottom: 2rem;
}
.company-portfolio__card img {
  width: 10rem;
  /* text-align: left; */
  border-radius: 4px;
}
.company-portfolio__card h4 {
  text-align: left;
  margin-top: 2rem;
}
.spaces-contact {
    margin-top: 2rem;
}
.contact {
    font-size: 2rem;
    font-weight: 600;
    text-decoration: none;
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
    z-index: 2;
    background: var(--semanticOne);
    box-shadow: 0px 1px 6px rgb(0 0 0 / 6%);
    border-radius: 6px;
  }
}
</style>

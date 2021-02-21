<template>
  <main id="home">
    <div class="hero-page section-container">
      <div class="hero-page__textbox">
        <div class="set-min-height">
          <h2>
            Empowering small merchants to grow big profits.
          </h2>
            <transition
            mode="out-in"
            enter-active-class="animate__animated animate__fadeIn">
              <p class="hero-page__brief" v-if="headerAnimationDone">
                Over
                <strong>100,000</strong>
                retailers have put their trust in Spaces to digitize and
                grow their business. 
                <strong>Track your sales</strong>,
                &nbsp;
                <strong>know your customers</strong>, and let
                Spaces help you access 
                <strong>finance, manage logistics, and reach a wider
                market</strong> 
              </p>
            </transition>
        </div>
        <p>
          <a class="app-link">
          Download App
            <i class="fas fa-external-link-square-alt"></i>
          </a>
        </p>
      </div>
      <div class="hero-page__carousel">
        <agile 
        :autoplay="true"
        :speed="1000"
        >
          <div class="hero-page__carousel__image">
            <img src="@/assets/images/homepage/merchant-in-shop.jpg" alt="Merchant in Shop" />
          </div>
          <div class="hero-page__carousel__image">
            <img src="@/assets/images/homepage/pepper-merchant.jpg" alt="Pepper Merchant" />
          </div>
          <div class="hero-page__carousel__image">
            <img src="@/assets/images/homepage/marketplace.jpg" alt="Marketplace" />
          </div>
        </agile>
      </div>
    </div>
  </main>
</template>

<script>
import IsMobile from "@/mixins/IsMobile";
import { VueAgile } from 'vue-agile'
import 'animate.css';


export default {
  name: 'Home',
  components: {
    agile: VueAgile,
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
      dataText: 'Empowering small merchants to grow big profits.',
      headerAnimationDone: false,
    };
  },
  beforeMount() {
    window.addEventListener("DOMContentLoaded", this.domLoaded);
  },
  methods: {
    domLoaded() {
      this.startTextAnimation();
    },
    typeWriter(text, i) {
      const self = this;
      if (i < text.length) {
        // add next character to h1
        document.querySelector("h2").innerHTML =
          text.substring(0, i + 1) + '<span aria-hidden="true"></span>';

        // wait for a while and call this function again for next character
        setTimeout(function() {
          self.typeWriter(text, i + 1);
        }, 80);
      }
      if (i === text.length) {
        this.headerAnimationDone = true;
      }
    },
    startTextAnimation() {
        // text exists! start typewriter animation
      this.typeWriter(this.dataText, 0);
    },
    animateButton() {
      this.animateButtonChevron = true;
    },
    removeButtonAnimation() {
      this.animateButtonChevron = false;
    },
  },
};
</script>

<style>
.agile__actions button {
  display: none;
}
</style>

<style scoped>
.hero-page__carousel__image {
  height: 40rem;
	object-fit: cover;
  width: 60rem;
}
.inline-paragraph {
  color: var(--primaryOne);
}
.hero-page__brief {
  padding: 3rem 0;
  font-size: 1.6rem;
  min-height: 15.6rem;
}
.s-button span {
  margin-left: -10px;
}
.app-link {
  font-size: 1.8rem;
}
.hero-page__textbox h2 {
  color: var(--primaryOne);
}
.app-link .fas {
  padding-left: 0.5rem;
}
.hero-page {
  margin-top: 10rem;
}
.hero-page__textbox {
  color: black;
  margin-bottom: 4rem;
}
.hero-page__carousel {
  max-width: 300px;
  margin: 0;
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
    display: flex;
    justify-content: space-between;
    margin-top: 8rem;
    padding-top: 5rem;
    padding-bottom: 5rem;
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
  .hero-page__textbox h2 {
    min-height: 14rem;
    color: var(--primaryOne);
  }
  .hero-page__carousel {
    max-width: 600px;
    margin: 0;
    min-height: 45rem;
    float: right;
  }
  .set-min-height {
    min-height: 29.6rem;
  }
  span {
    border-right: 0.05em solid;
    animation: caret 1s steps(1) infinite;
  }

  @keyframes caret {
    50% {
      border-color: transparent;
    }
  }
}
@media screen and (max-width: 767px) {
  main {
    min-height: auto;
  }
}
</style>

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
        <!-- <button v-if="!isMobile" class="s-button" @mouseover="animateButton" @mouseleave="removeButtonAnimation">
            <p class="button__text" :class="{'animate-btn-text' : animateButtonChevron}">Download App</p>
            <i class="fas fa-external-link-square-alt" :class="{'chevron-r' : animateButtonChevron}"></i>
        </button>
        <a class="app-link" v-else>
         <span>Download App</span>
          <i class="fas fa-external-link-square-alt"></i>
        </a> -->
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
      dataText: [ 
        "Empowering small merchants to grow big profits." 
        ],
    };
  },
  beforeMount() {
    window.addEventListener("DOMContentLoaded", this.domLoaded);
  },
  methods: {
    domLoaded() {
      this.startTextAnimation(0);
    },
    typeWriter(text, i, fnCallback) {
      const self = this;
      if (i < (text.length)) {
        // add next character to h1
       document.querySelector("h2").innerHTML = text.substring(0, i+1) +'<span aria-hidden="true"></span>';
  
        // wait for a while and call this function again for next character
        setTimeout(function() {
          self.typeWriter(text, i + 1, fnCallback)
        }, 80);
      }
      else if (typeof fnCallback == 'function') {
        // call callback after timeout
        setTimeout(fnCallback, 1500);
      }
    },
    startTextAnimation(i) {
      const self = this;
      if (typeof this.dataText[i] == 'undefined'){
        setTimeout(function() {
          self.startTextAnimation(0);
        }, 20000);
      }
      if (i < this.dataText[i].length) {
        // text exists! start typewriter animation
       this.typeWriter(this.dataText[i], 0, function(){
         // after callback (and whole text has been animated), start next text
         self.startTextAnimation(i + 1);
       });
      }
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

<style scoped>
.s-button {
    width: 100%;
    max-width: 34.6rem;
    height: 7.4rem;
    background: white;
    color: var(--primaryOne);
    font-size: 2.8rem;
    font-weight: 300;
    position: relative;
}
.button__text {
  display: inline;
  margin: 0;
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
.fa-external-link-square-alt {
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
    .hero-page__textbox h2{
      min-height: 14rem;
    }
    .hero-page__carousel {
        max-width: 600px;
        margin: 0;
        min-height: 45rem;
        display: flex;
        flex-wrap: wrap;
        align-content: flex-end;
    }
    span {
      border-right: .05em solid;
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

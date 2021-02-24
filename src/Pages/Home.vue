<template>
  <main id="home">
    <div class="hero-page section-container">
      <div class="hero-page__textbox">
        <div>
          <h2>
            Empowering small merchants to grow big profits. 
          </h2>
          <div class="hero-page__carousel-parent">
          <transition
            mode="out-in"
            enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="hero-page__carousel" v-if="IsPhone && headerAnimationDone">
              <agile 
              :autoplay="true"
              :speed="1000"
              >
                <div class="hero-page__carousel__image">
                  <img src="@/assets/images/homepage/merchant-with-app.jpeg" alt="Merchant with app" />
                </div>
                <div class="hero-page__carousel__image">
                  <img src="@/assets/images/homepage/merchant-in-shop.jpg" alt="Pepper Merchant" />
                </div>
                <div class="hero-page__carousel__image">
                  <img src="@/assets/images/homepage/cobbler.jpg" alt="Cobbler" />
                </div>
              </agile>
            </div>
          </transition>
          </div>
            <transition
            mode="out-in"
            enter-active-class="animate__animated animate__fadeInLeft">
              <p class="hero-page__brief" v-if="headerAnimationDone">
                Over
                  <ICountUp
                    :delay="delay"
                    :endVal="endVal"
                    :duration="200"
                    :options="options"
                    @ready="onReady"
                  />
                  merchants have put their trust in Spaces to grow their business and increase their income.<br>
                  <br>
                  Spaces helps you track your sales, provide insights on your customers, and manage logistics all
                  while providing access to finance a broader market for your products.
              </p>
            </transition>
        </div>
        <transition
            mode="out-in"
            enter-active-class="animate__animated animate__fadeInLeftBig"
        >
        <p v-show="headerAnimationDone" class="button-block">
          <a class="s-button" target="_blank" href="http://onelink.to/qahauh">
          Download App
          </a>
        </p>
        </transition>
      </div>
      <div class="hero-page__carousel-parent">
        <transition            
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        >
          <div class="hero-page__carousel" v-if="!IsPhone && headerAnimationDone">
            <agile 
            :autoplay="true"
            :speed="1000"
            >
              <div class="hero-page__carousel__image">
                <img src="@/assets/images/homepage/merchant-with-app.jpeg" alt="Merchant with spaces app" />
              </div>
              <div class="hero-page__carousel__image">
                <img src="@/assets/images/homepage/merchant-in-shop.jpg" alt="Pepper Merchant" />
              </div>
              <div class="hero-page__carousel__image">
                <img src="@/assets/images/homepage/cobbler.jpg" alt="cobbler" />
              </div>
            </agile>
          </div>
        </transition>
      </div>
    </div>
  </main>
</template>

<script>
import ICountUp from 'vue-countup-v2';
import IsPhone from "@/mixins/IsPhone";
import { VueAgile } from 'vue-agile'
import 'animate.css';


export default {
  name: 'Home',
  components: {
    agile: VueAgile,
    ICountUp,
  },
  mixins: [IsPhone],
  data() {
    return {
      dataText: 'Empowering small merchants to grow big profits.',
      headerAnimationDone: false,
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
    window.addEventListener("DOMContentLoaded", this.domLoaded);
  },
  methods: {
    onReady: function(instance) {
      const that = this;
      instance.update(that.endVal + 0);
    },
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
        setTimeout(() => {
          this.startTextAnimation();
        }, 3000);
      }
    },
    startTextAnimation() {
        // text exists! start typewriter animation
      this.typeWriter(this.dataText, 0);
    },
  },
};
</script>

<style>
.agile {
  width: 100%;
}
.agile__actions {
	margin-top: 20px;
  text-align: center;
}
.agile__nav-button {
		background: transparent;
		border: none;
		color: #ccc;
		cursor: pointer;
		font-size: 24px;
		transition-duration: .3s;
}
.agile__nav-button:hover {
			color: var(--typeOne);
}
.agile__dot {
  margin: 0 10px;
}
.agile__dot button {
			background-color: #eee;
			border: none;
			border-radius: 50%;
			cursor: pointer;
			height: 10px;
			font-size: 0;
			line-height: 0;
			margin: 0;
			padding: 0;
			transition-duration: .3s;
			width: 10px;
}
.agile__dot--current button {
	background-color: var(--typeOne);
  border-radius: 50%;
}
.agile__dot--current, .agile__dot:hover {
	background-color: var(--typeOne);
  border-radius: 50%;
}
.slide {
	align-items: center;
	color: #fff;
	display: flex;
	height: 30rem;
	justify-content: center;
}

.agile__nav-button {
  display: none;
}
.agile__dots {
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  list-style: none;
  width: 100%;
  justify-content: center;
  padding: 0;
  white-space: nowrap;
}

</style>

<style scoped>
.hero-page__carousel__image {
  max-height: 40rem;
	object-fit: cover;
  max-width: 60rem;
}
.hero-page__brief {
  color: var(--primaryTwo);
  padding: 3rem 0;
  margin: 0;
  line-height: 1.2;
  font-size: 1.6rem;
  font-weight: 500;
}
.s-button {
  line-height: 1.7;
}
.hero-page__brief span {
  min-width: 6rem;
  display: inline-block;
}
.hero-page__textbox h2 {
  min-height: 10.2rem;
  margin-bottom: 2rem;
}
.hero-page {
  margin-top: 10rem;
}
.hero-page__textbox {
  color: black;
  margin-bottom: 6rem;
}
.hero-page__carousel-parent {
  position: relative;
}
.hero-page__carousel::before {
  display: block;
  content: "";
  width: 306px;
  height: 206px;
  border: 2px solid var(--typeOne);
  position: absolute;
  top: -3px;
  left: -3px;
  border-radius: 4px;
  z-index: -1;
}
.hero-page__carousel__image img {
  z-index: 5;
  height: 40rem;
}
.button-block {
  margin-top: 2rem;
}
@media screen and (min-width: 768px) {
  .hero-page {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 9rem;
    min-height: 50rem;
    padding-bottom: 5rem;
  }
  .hero-page__carousel-parent {
    width: 50%;
  }
  .hero-page__brief {
    padding: 1rem 0 1rem;
    font-size: 1.6rem;
    background: var(--neutralTwo);
    box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
    border-radius: 10px;
  }
  .hero-page__carousel::before {
    display: block;
    content: "";
    width: 102%;
    max-width: 61rem;
    max-height: 41rem;
    height: 100%;
    border: 4px solid var(--typeOne);
    position: absolute;
    top: -5px;
    left: -5px;
    border-radius: 4px;
    z-index: -1;
  }
  .hero-page__textbox {
    color: black;
    max-width: 40%;
    margin-bottom: 4rem;
  }
  .hero-page__textbox h2 {
    min-height: 6.4rem;
  }
  .hero-page__carousel {
    width: 100%;
    max-width: 60rem;
    margin: 0;
    min-height: 45rem;
  }
  h2 span {
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
    min-height: 60rem;
  }
  .section-container {
    padding-bottom: 0;
  }
  .hero-page__carousel__image {
    height: auto;
    object-fit: cover;
  }
  .hero-page__carousel__image img {
    height: 20rem;
  }
  .hero-page__carousel {
    max-width: 30rem;
  }  
}
</style>

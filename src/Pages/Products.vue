<template>
  <main id="products">
    <div class="products-section section-container">
      <div class="products-section__textbox">
        <h2>All the products in one easy to use
          <transition>
            <span class="animate__animated animate__tada" v-if="runanimation">
              app!
            </span>
          </transition>
          </h2>
        <section class="products-grid">
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item" v-show="showMyShop">
              <img src="@/assets/images/product-icons/myshop.svg" alt="MyShop Icon" class="products-item__image" />
              <figcaption>Myshop</figcaption>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item" v-show="showMerchBuy">
              <img src="@/assets/images/product-icons/merchbuy.svg" alt="MerchBuy Icon" class="products-item__image" />
              <figcaption>Merchbuy</figcaption>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item" v-show="showMerchlist">
              <img src="@/assets/images/product-icons/merchlist.svg" alt="Merchlist Icon" class="products-item__image" />
              <figcaption>Merchlist</figcaption>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item" v-show="showWarenext">
              <img src="@/assets/images/product-icons/warenext.svg" alt="Warenext Icon" class="products-item__image" />
              <figcaption>Warenext</figcaption>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item" v-show="showAgencyBanking">
              <img src="@/assets/images/product-icons/agency-banking.svg" alt="Agency Banking Icon" class="products-item__image" />
              <figcaption>Agency Banking</figcaption>
            </div>
          </transition>
        </section>
        <a class="app-link" target="_blank" href="http://onelink.to/qahauh"> 
          <span>Download App</span>
          <i class="fas fa-external-link-square-alt"></i>
        </a>
      </div>
      <div class="products-image">
        <img src="@/assets/images/spaces-user.jpeg" alt="" />
      </div>
    </div>
  </main>
</template>

<script>
import 'animate.css';

export default {
  name: 'products',
  data() {
    return {
      runanimation: false,
      showMyShop: false,
      showMerchBuy: false,
      showMerchlist: false,
      showWarenext: false,
      showAgencyBanking: false,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  watch: {
    runanimation(value) {
      if (value) {
        this.showMyShop = true;
        setTimeout(() => {
          this.showMerchBuy = true;
        }, 80);
        setTimeout(() => {
          this.showMerchlist = true;
        }, 240);
        setTimeout(() => {
          this.showWarenext = true;
        }, 360);
        setTimeout(() => {
          this.showAgencyBanking = true;
        }, 480);
      }
    }
  },
  methods: {
    checkOffset() {
      console.log(window.pageYOffset);
    },
    handleScroll() {
      if (window.pageYOffset > 490) {
        this.runanimation = true;
      }
    },
  }
};
</script>

<style scoped>
.s-button {
  width: 28rem;
}
.products-section {
  padding-top: 5rem;
  padding-bottom: 5rem;
}
.products-image {
  max-width: 250px;
}
.products-item {
  text-align: center;
  margin-bottom: 2rem;
  margin-right: 1.3rem;
}
.products-item__image {
  /* width: 100px; */
  border-radius: 12px;
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
  border: 0.3px solid var(--semanticFive);
}
.products-item__image:hover {
  box-shadow: 0px 5px 10px rgb(0 0 0 / 2%);
}
.products-item figcaption {
  font-size: 1.4rem;
}
.products-grid {
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 5rem 0 3rem;
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
@media screen and (min-width: 768px) {
  .products-section {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 5rem;
    padding-bottom: 5rem;
  }
  .products-item:hover {
    font-weight: 600;
  }
  .products-item__image {
    width: auto;
  }
  .products-item__image:hover {
    box-shadow: 5px 5px 10px rgb(0 0 0 / 2%);
  }
  .products-item {
    margin-right: 4rem;
  }
  .products-section__textbox {
    max-width: 50rem;
  }
  .products-image {
    max-width: 600px;
    height: 450px;
    overflow: hidden;
  }
  .products-grid {
    display: inline-flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 5rem 0;
    min-height: 38rem;
  }
  @keyframes float {
    
  }
}
@media screen and (max-width: 767px) {
  .app-link {
    display: block;
    text-align: center;
  }
  .products-image {
    margin: 2rem auto 0;
  }
}
</style>

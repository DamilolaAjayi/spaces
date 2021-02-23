<template>
  <main id="products">
    <div class="products-section section-container">
      <div class="products-section__textbox">
        <h3>
          All the products in one easy to use App!
        </h3>
        <section class="products-grid">
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item">
              <img src="@/assets/images/product-icons/myshop.svg" alt="MyShop Icon" class="products-item__image" />
              <figcaption>Myshop</figcaption>
              <p>Store management software for micro and small enterprises to track daily business transactions – sales, debts, inventory; helping them grow their profits faster</p>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item">
              <img src="@/assets/images/product-icons/merchbuy.svg" alt="MerchBuy Icon" class="products-item__image" />
              <figcaption>Merchbuy</figcaption>
              <p>B2B trade platform connecting manufacturers, distributors, retailers, and wholesalers while offering secure payments and hassle-free logistics</p>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item">
              <img src="@/assets/images/product-icons/merchlist.svg" alt="Merchlist Icon" class="products-item__image" />
              <figcaption>Merchlist</figcaption>
              <p>Automates online listings of merchant’s inventory via a consumer-facing website, growing demand and revenue for them</p>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item">
              <img src="@/assets/images/product-icons/agency-banking.svg" alt="Agency Banking Icon" class="products-item__image" />
              <figcaption>Agency Banking</figcaption>
              <p>Enabling agents earn money by offering financial services in their communities </p>
            </div>
          </transition>
          <transition
          mode="out-in"
          enter-active-class="animate__animated animate__fadeIn"
          >
            <div class="products-item">
              <img src="@/assets/images/product-icons/warenext.svg" alt="Warenext Icon" class="products-item__image" />
              <figcaption>Warenext</figcaption>
              <p>Logistics marketplace that allows users see and understand the cost of moving goods from one location and so conduct logistics part of their business easily</p>
            </div>
          </transition>
        </section>
        <div class="button-block">
          <a class="s-button" target="_blank" href="http://onelink.to/qahauh">
          Download App
          </a>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import 'animate.css';

export default {
  name: 'products',
};
</script>

<style scoped>
.products-section {
  padding-top: 3rem;
  padding-bottom: 3rem;
}
.products-image {
  max-width: 250px;
  overflow: hidden;
  border-radius: 6px;
  box-shadow: 0px 1px 6px rgb(0 0 0 / 8%);
}
.products-item {
  text-align: left;
  margin-bottom: 2rem;
  max-width: 23rem;
  padding: 1rem;
  width: 100%;
  z-index: 8;
  border: 0.5px solid rgba(34, 168, 255, 0.3);
  border-radius: 4px;
  box-sizing: content-box;
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
}
.products-item__image {
  border-radius: 12px;
  object-fit: cover;
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
}
.products-item__image:hover {
  box-shadow: 0px 5px 10px rgb(0 0 0 / 2%);
}
.products-section__textbox h3 {
  text-align: center;
}
.products-item figcaption {
  font-size: 1.4rem;
  margin-top: 0.4rem;
  border-bottom: 0.5px solid var(--typeOne);
  padding-bottom: 0.2rem;
  width: max-content;
}
.button-block {
  text-align: center;
  margin: 1rem;
}
.s-button {
  line-height: 1.7;
  margin: 0 auto;
}
@media screen and (min-width: 768px) {
  .products-item:hover {
    font-weight: 600;
  }
  .products-item__image {
    width: auto;
  }
  .products-item__image:hover {
    box-shadow: 5px 5px 10px rgb(0 0 0 / 2%);
  }
  p {
    text-align: left;
  }
  .products-image {
    max-width: 600px;
    height: 450px;
  }
  .products-grid {
    display: grid;
    grid-template-columns: auto auto auto auto auto;
    grid-column-gap: 3rem;
    width: 100%;
    padding: 3rem 0 0;
  }
}
@media screen and (max-width: 767px) {
  .products-image {
    margin: 5rem auto 0;
  }
  .products-grid {
    display: inline-flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 3rem 0 1rem;
  }
}
</style>

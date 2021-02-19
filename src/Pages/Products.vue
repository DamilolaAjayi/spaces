<template>
  <main id="products" class="products-section section-container">
    <div class="products-section__textbox">
      <h2>All the products in one easy to use app!</h2>
      <section class="products-grid">
        <div class="products-item" @mouseover="boldenText">
          <img src="http://placehold.it/100x100" alt="MyShop Icon" />
          <figcaption>Myshop</figcaption>
        </div>
        <div class="products-item" @mouseover="boldenText">
          <img src="http://placehold.it/100x100" alt="MerchBuy Icon" />
          <figcaption>Merchbuy</figcaption>
        </div>
        <div class="products-item" @mouseover="boldenText">
          <img src="http://placehold.it/100x100" alt="Merchlist Icon" />
          <figcaption>Merchlist</figcaption>
        </div>
        <div class="products-item" @mouseover="boldenText">
          <img src="http://placehold.it/100x100" alt="Warenext Icon" />
          <figcaption>Warenext</figcaption>
        </div>
        <div class="products-item" @mouseover="boldenText">
          <img src="http://placehold.it/100x100" alt="Agency Banking Icon" />
          <figcaption>Agency Banking</figcaption>
        </div>
      </section>
      <a class="app-link">
        <span>Download App</span>
        <i class="fas fa-external-link-square-alt"></i>
      </a>
    </div>
    <div class="products-image">
      <img src="http://placehold.it/600x400" alt="" />
    </div>
  </main>
</template>

<script>
export default {
  name: 'products',
  methods: {
    boldenText() {
      console.log(this);
    },
  }
};
</script>

<style scoped>
.s-button {
  width: 28rem;
}
.products-image {
  max-width: 250px;
}
.products-item {
  text-align: center;
  margin-bottom: 2rem;
  margin-right: 1.3rem;
}
.products-item img {
  width: 100px;
  border: 0.2px solid var(--semanticFive);
}
.products-item figcaption {
  font-size: 1.4rem;
}
.products-grid {
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: space-around;
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
  }
  .products-item img {
    width: auto;
  }
  .products-item {
    margin-right: 4rem;
  }
  .products-item:hover {

  }
  .products-section__textbox {
    max-width: 50rem;
  }
  .products-image {
    max-width: 600px;
  }
  .products-grid {
    display: inline-flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    padding: 5rem 0;
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

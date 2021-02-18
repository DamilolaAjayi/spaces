<template>
  <main id="products" class="products-section">
    <div>
      <h2>All the products in one easy to use app!</h2>
      <section class="products-grid">
        <div class="products-item">
          <figcaption>Myshop</figcaption>
        </div>
        <div class="products-item">
          <figcaption>Merchbuy</figcaption>
        </div>
        <div class="products-item">
          <figcaption>Merchlist</figcaption>
        </div>
        <div class="products-item">
          <figcaption>Warenext</figcaption>
        </div>
        <div class="products-item">
          <figcaption>Agency Banking</figcaption>
        </div>
      </section>
      <button class="s-button">Download App</button>
    </div>
    <div class="products-image">
      <img src="http://placehold.it/600x400" alt="" />
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
/* .products-section {
    flex-direction: column;
} */
.s-button {
    width: 28rem;
}
.products-image {
    max-width: 250px;
}
@media screen and (min-width: 768px) {
    .products-section {
        display: flex;
        justify-content: space-between;
    }
    .products-image {
        max-width: 600px;
    }
    .products-grid {
        display: flex;
    }
}
</style>

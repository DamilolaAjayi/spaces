<template>
  <main id="home">
      <div class="hero-page">
        <div class="hero-page__textbox">
        <h2>
            Empowering small merchants to grow big profits.
        </h2>
        <p>
            Over 100,000 retailers have put their trust in Spaces to digitize their
            business. Spaces helps you track your sales and customers, provide a
            broader assortment for your clients, facilitate access to finance,
            manage your logistics and grow your business quickly.
        </p>
        </div>
        <div class="">
        <img src="http://placehold.it/600x400" alt="" />
        </div>
      </div>
  </main>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            data: [
                '<img src="http://placehold.it/600x400" alt="" />',
                '<img src="http://placehold.it/600x400" alt="" />',
                '<img src="http://placehold.it/600x400" alt="" />',
            ],
        };
    },
};
</script>

<style scoped>
    .hero-page {
        display: flex;
        justify-content: space-between;
        margin-top: 80px;
    }
    .hero-page__textbox {
        color: black;
    }
</style>

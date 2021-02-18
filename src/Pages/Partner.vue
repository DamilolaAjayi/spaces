<template>
  <section class="company-about__section">
      <header class="company-about__header">
        <h2>Do you want to Partner with us?</h2>
        <h3>
        We have an unparalleled understanding of the
        <a
            target="_blank"
            href="https://www.boi.ng/wp-content/uploads/2018/05/BOI-Working-Paper-Series-No2_Economic-Development-through-the-Nigerian-Informal-Sector-A-BOI-perspective.pdf"
        >
            <span>informal sector</span>
        </a>
        </h3>
      </header>
    <div class="company-portfolio">
      <div class="company-portfolio__card"></div>
      <div class="company-portfolio__card"></div>
      <div class="company-portfolio__card"></div>
      <div class="company-portfolio__card"></div>
    </div>
    <div>
      <a target="_blank" :href="`mailto:info@spaces.io`" class="contact"
        >info@spaces.io</a
      >
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.company-about__header {
    margin-bottom: 2rem;
}
.company-about__section {
  text-align: center;
}
.company-portfolio__card {
  overflow: hidden;
  height: 250px;
  width: 250px;
  margin: 0 auto;
  z-index: 2;
  background: var(--semanticOne);
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
  border-radius: 6px;
  margin-bottom: 2rem;
}
@media screen and (min-width: 768px) {
  .company-portfolio {
    display: flex;
    justify-content: space-between;
  }
  .company-portfolio__card {
    overflow: hidden;
    height: 250px;
    width: 250px;
    z-index: 2;
    background: var(--semanticOne);
    box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
    border-radius: 6px;
  }
}
</style>

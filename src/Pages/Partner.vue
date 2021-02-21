<template>
  <section class="company-about__section section-container" id="partner">
      <header class="company-about__header">
        <h2>Do you want to Partner with us?</h2>
        <h3>
        We have an unparalleled understanding of the
        <a
            target="_blank"
            href="https://www.boi.ng/wp-content/uploads/2018/05/BOI-Working-Paper-Series-No2_Economic-Development-through-the-Nigerian-Informal-Sector-A-BOI-perspective.pdf"
        >
            informal sector
        </a>
        </h3>
      </header>
    <div class="company-portfolio">
      <div class="company-portfolio__card">
          <h4>
              You have a product or service you want to provide to [ticking dynamic count of registered merchants? ]  merchants?
          </h4>
      </div>
      <div class="company-portfolio__card">
          <h4>
              You want to track performance and preferences for your product or service?
          </h4>
      </div>
      <div class="company-portfolio__card">
          <h4>
              Largest informal distribution channel in Africa. 
          </h4>
      </div>
      <div class="company-portfolio__card">
          <h4>
              100k active merchants, 10,000 agents across Nigeria, $1.5 billion in recorded sales
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
export default {};
</script>

<style scoped>
.company-about__header {
    margin-bottom: 2rem;
}
.company-about__header h3 {
    margin: 4rem 0;
    opacity: 0.7;
}
.company-about__section {
  text-align: center;
  background: var(--semanticOne);
}
.company-portfolio__card {
  overflow: hidden;
  display: flex;
  align-items: center;
  padding: 0 2rem;
  height: 250px;
  width: 250px;
  margin: 0 auto;
  z-index: 2;
  background: var(--semanticOne);
  box-shadow: 0px 1px 6px rgb(0 0 0 / 2%);
  border-radius: 6px;
  margin-bottom: 2rem;
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

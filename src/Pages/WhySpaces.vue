<template>
  <main id="purpose" :class="{'modal-is-open' : openModal}">
    <div class="company section-container">
      <header class="purpose__header">
        <h3>Why Use Spaces?</h3>
        <img class="purpose__header-image" src="https://ik.imagekit.io/7dkc9ii1v1r/Underline-5-Blue_FOHOHoKip.png" alt="blue underline image">
      </header>
      <div class="company-purpose" v-if="!isMobile">
        <agile
          :autoplay="true"
          :speed="1000"
        >
        <div class="group">
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/increase-demand-1_3aGdjgyCjoug.svg" alt="increase goods demand" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/improvecash-flows-1_eKS7G5nGn.svg" alt="improve merchant cashflow" />
              </div>
            </div>
        </div>
        <div class="group">
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/streamlined-logistics-1_ttVtRRTjl.svg" alt="streamlined logistics" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/automatic-savings-1_H2xw13uK3wRw.svg" alt="automatic savings" />
              </div>
            </div>
        </div>
        </agile>
      </div>
      <div v-else>
        <agile
          :autoplay="true"
          :speed="1000"
        >
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/increase-demand-1_3aGdjgyCjoug.svg" alt="increase goods demand" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/improvecash-flows-1_eKS7G5nGn.svg" alt="improve merchant cashflow" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/streamlined-logistics-1_ttVtRRTjl.svg" alt="streamlined logistics" />
              </div>
            </div>
            <div class="company-purpose__block">
              <div class="company-purpose-block__image">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/automatic-savings-1_H2xw13uK3wRw.svg" alt="automatic savings" />
              </div>
            </div>
        </agile>
      </div>
    </div>
  </main>
</template>

<script>
import IsMobile from "@/mixins/IsMobile";
import { VueAgile } from 'vue-agile'

export default {
  name: 'why-spaces',
  props: {
    openModal: Boolean,
  },
  components: {
    agile: VueAgile,
  },
  mixins: [IsMobile],
};
</script>

<style scoped>
  .group {
    display: flex;
  }
  .section-container {
    background-color: var(--semanticTwo);
  }
  .purpose__header {
    margin-bottom: -2rem;
  }
    main {
        min-height: auto;
    }
    .purpose__header-image {
      height: 2.5rem;
      width: 20rem;
      margin-top: -8px;
    }
    .company-purpose__block {
      display: flex;
      width: 100%;
      flex-direction: column;
      justify-content: center;
    }
    .company-purpose__textbox h3 {
      font-weight: 400;
      font-size: 2rem;
    }
    .company-purpose-block__image {
      width: 28rem;
    }
@media screen and (min-width: 768px) {
  .section-container {
  padding-top: 5rem;
  padding-bottom: 5rem;
}
.company {
  text-align: center;
}
.purpose__header {
  width: max-content;
  margin: 0 auto 4rem auto;
  max-width: 100%;
}
.purpose__header-image {
    width: 25rem;
}
.company-purpose {
  margin: 0 auto;
  max-width: 90%;
}
.company-purpose__block {
  display: flex;
  width: 100%;
  position: relative;
}
.company-purpose__textbox {
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
  color: var(--primaryTwo);
}
.company-purpose__textbox h3 {
  font-weight: 600;
  font-size: 4rem;
  color: var(--primaryFour);
}
.company-purpose__brief {
  font-size: 2rem;
  font-weight: 400;
}
.company-purpose-block__image {
  width: 100%;
  max-height: 35rem;
  height: 35rem;
  border: 5px solid var(--semanticFour);
  overflow: hidden;
}
}
@media screen  and (max-width: 767px) {
  .section-container {
    text-align: center;
    padding-top: 3rem;
    padding-bottom: 4rem;
    width: 100%;
  }
  .company-purpose__block {
    align-items: center;
    padding: 4rem 0 0;
  }
  .company-purpose__textbox {
    margin-top: 0.5rem;
  }
  .company-purpose-block__image {
    box-shadow: 0px 1px 6px rgb(0 0 0 / 8%);
  }
  .company-purpose-block__image img {
    border-radius: 6px;
  }
  .company-purpose__textbox h3 {
    padding-bottom: 0.5rem;
    border-bottom: 0.5px solid var(--typeOne);
  }
}
</style>

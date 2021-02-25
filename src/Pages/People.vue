<template>
  <section id="people" class="team section-container" :class="{'modal-is-open' : openModal}">
    <header class="people">
      <h3 class="team__header">Team</h3>
      <img src="https://ik.imagekit.io/7dkc9ii1v1r/Underline-5-Blue_FOHOHoKip.png" alt="" class="header__underline">
    </header>
    <div class="team-container">
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/anu-adasolum_tV2DpZcFw.jpeg"
          alt="Spaces CEO Anu Adasolum"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Anu Adasolum
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/anu-adasolum-46754a19/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Co-Founder &amp; CEO</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/funto-faleye_XdlXInvgq.jpg"
          alt="Spaces COO Funto Faleye"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Funto Faleye
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/funto-faleye-b08a4059/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Chief Operating Officer</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/abimbola-dasilva_-7CtM5y8t.jpg"
          alt="Abimbola Dasilva Spaces Head of Business Intelligence &amp; Customer Experience"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Abimbola Dasilva
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/da-silva-abimbola-566a525b/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of Business Intelligence &amp; Customer Experience</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/adegbenga-adeye_ZE5qJ5C44.jpg"
          alt="Adegbenga Adeye Spaces CTO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Adegbenga Adeye
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/adegbenga-adeye-psm-i-14003635/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Chief Technology Officer</p>
        </div>
      </div>
    </div>
    <div class="team-container">
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/afolashakin-ajayi_DoeUY91k5pQ8.jpeg"
          alt="Afolashakin Ajayi Spaces Head of Product"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Afolashakin Ajayi
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/afolashakinajayi/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of Product</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/edidiong-uwemakpan_o6t7EsyOU4fG.jpeg"
          alt="Edidiong Uwemakpan Spaces Head of Marketing"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
          <span>
            Edidiong Uwemakpan
          </span>
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/didiuwem/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of Marketing</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/omokhafe-dirisu_ZY9dZnkmu.jpeg"
          alt="Omokhafe Dirisu Spaces CCO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Omokhafe Dirisu
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/omokhafe-dirisu-25119747/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Chief Commercial Officer</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="https://ik.imagekit.io/7dkc9ii1v1r/ademola-adesina_AoyRZGl_d.jpg"
          alt="Ademola Adesina Spaces CCO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Ademola Adesina
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/aadesina/">
                <img src="https://ik.imagekit.io/7dkc9ii1v1r/linkedin-logo_NbOm3DVKG.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Co-Founder &amp; President</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'people',
  props: {
    openModal: Boolean,
  },
};
</script>

<style scoped>
.team {
  text-align: center;
}
.team__header {
  width: max-content;
  margin: 0 auto;
}
.team-container {
  text-align: center;
}
.team-member {
  width: 20rem;
  margin: 0 auto 3rem;
}
  .team-member-card span {
    margin-right: -8px;
    width: 35px;
  }
  .team-member__image {
    border-radius: 2rem;
    margin-bottom: 2rem;
    object-fit: cover;
    height: 200px;
    width: 200px;
    box-shadow: 1px 1px 6px rgb(0 0 0 / 15%);
    position: relative;
  }
  .header__underline {
      height: 2.5rem;
      width: 10rem;
      margin-top: -8px;
  }
  .people {
    margin-bottom: 2rem;
  }
  .team-member-card__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .team-member-card span img {
    width: 100%;
  }
  .team-member-card__role {
    margin-top: 0.2rem;
  }
@media screen and (min-width: 768px) {
  .team {
    padding-top: 5rem;
    padding-bottom: 5rem;
  }
  .team-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .team-member-card span {
    margin-right: -8px;
    width: 35px;
  }
  .team-member__image {
    border-radius: 20px;
    margin-bottom: 2rem;
  }
  .team-member-card__role {
    font-size: 1.4rem;
    margin: 0;
    text-align: left;
    font-weight: 400;
  }
  .team-member-card__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .team-member-card span img {
    width: 100%;
  }
}
@media screen and (max-width: 767px) {
  .team {
    padding-top: 3rem;
    padding-bottom: 4rem;
  }
  .team-member__image {
    box-shadow: 1px 1px 4px #8C7B7B;
  }
  .team-member-card__role {
    width: max-content;
    max-width: 20rem;
    text-align: left;
  }
}
</style>

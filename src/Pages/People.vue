<template>
  <section id="people" class="team section-container">
    <header class="people">
      <h3 class="team__header">Executive team</h3>
      <img src="@/assets/Underline-5-Blue.png" alt="" class="header__underline">
    </header>
    <div class="team-container">
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/anu-adasolum.jpg"
          alt="Spaces CEO Anu Adasolum"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Anu Adasolum
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/anu-adasolum-46754a19/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">CEO</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/funto-faleye.jpg"
          alt="Spaces COO Funto Faleye"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Funto Faleye
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/funto-faleye-b08a4059/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">COO</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/abimbola-dasilva.jpeg"
          alt="Abimbola Dasilva Spaces Head of BI &amp; Customer Service"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Abimbola Dasilva
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/adegbenga-adeye-psm-i-14003635/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of BI & Customer Service</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/adegbenga-adeye.jpg"
          alt="Adegbenga Adeye Spaces CTO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Adegbenga Adeye
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/adegbenga-adeye-psm-i-14003635/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">CTO</p>
        </div>
      </div>
    </div>
    <div class="team-container team-container-2">
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/afolashakin-ajayi.jpeg"
          alt="Afolashakin Ajayi Spaces Head of Products"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Afolashakin Ajayi
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/adegbenga-adeye-psm-i-14003635/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of Products</p>
        </div>
      </div>
      <div class="team-member head-marketing">
        <img
          class="team-member__image"
          src="@/assets/images/people/edidiong-uwemakpan.jpeg"
          alt="Edidiong Uwemakpan Spaces Head of Marketing"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Edidiong Uwemakpan
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/adegbenga-adeye-psm-i-14003635/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">Head of Marketing</p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="@/assets/images/people/omokhafe-dirisu.jpeg"
          alt="Omokhafe Dirisu Spaces CCO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Omokhafe Dirisu
            <span>
              <a target="_blank" href="https://www.linkedin.com/in/omokhafe-dirisu-25119747/">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p class="team-member-card__role">CCO</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'people',
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
.head-marketing {
  width: 25rem;
}
.team-member:nth-child(1) .team-member__image {
  animation-delay: 5ms;
}
.team-member:nth-child(2) .team-member__image {
  animation-delay: 1000ms;
}
.team-member:nth-child(3) .team-member__image {
  animation-delay: 5ms;
}
.team-member:nth-child(4) .team-member__image {
  animation-delay: 1000ms;
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
    box-shadow: 1px 1px 6px rgb(8 158 255 / 15%);
    animation: float 1.5s;
    position: relative;
    animation-delay: 5ms;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
  }
  .header__underline {
      height: 2.5rem;
      width: 20rem;
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
  @keyframes float {
    0% {
      top: 0px;
    }
    50% {
      top: 5px;
    }
    100% {
      top: 0px;
    }
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
  .team-container-2 {
    max-width: 80%;
    margin: 0 auto;
  }
  .team-member-card__role {
    font-size: 1.4rem;
    font-weight: 500;
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
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
  .team-member__image {
    box-shadow: 1px 1px 4px #8C7B7B;
  }
}
</style>

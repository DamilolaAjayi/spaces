<template>
  <section id="people" class="team section-container">
    <h2 class="team__header">Executive team</h2>
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
  margin-bottom: 3rem;
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
  .team__header {
    margin-bottom: 7rem;
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
    opacity: 0.7;
    font-weight: 400;
  }
  .team-member-card__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-weight: 500;
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
}
</style>

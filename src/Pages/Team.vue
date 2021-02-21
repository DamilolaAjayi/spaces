<template>
  <section id="team" class="team section-container">
    <h2 class="team__header">Meet our team</h2>
    <div class="team-container">
      <div class="team-member">
        <img
          class="team-member__image"
          src="http://placehold.it/277x277"
          alt="Spaces CEO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Lorem Ipsum
            <span>
              <a href="#">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p></p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="http://placehold.it/277x277"
          alt="Spaces COO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Lorem Ipsum
            <span>
              <a href="#">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p></p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="http://placehold.it/277x277"
          alt="Spaces CTO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Lorem Ipsum
            <span>
              <a href="#">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p></p>
        </div>
      </div>
      <div class="team-member">
        <img
          class="team-member__image"
          src="http://placehold.it/277x277"
          alt="Spaces CMO"
        />
        <div class="team-member-card">
          <h4 class="team-member-card__header">
            Lorem Ipsum
            <span>
              <a href="#">
                <img src="@/assets/linkedin-logo.png" alt="" />
              </a>
            </span>
          </h4>
          <p></p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "spaces-team",
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
    border-radius: 50%;
    margin-bottom: 2rem;
    object-fit: cover;
  }
  .team-member-card__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .team-member-card span img {
    width: 100%;
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
  .team-member-card__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .team-member-card span img {
    width: 100%;
  }
}
</style>

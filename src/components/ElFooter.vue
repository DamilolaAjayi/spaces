<template>
  <footer class="footer">
    <div class="footer__press">
      <img src="@/assets/spaces-lg.png" alt="spaces logo" class="footer-press__spaces-logo">
      <section>
        <h4>In the press</h4>
        <div class="footer__media">
          <a target="_blank" href="http://venturesafrica.com/rensource-launches-platform-to-connect-retailers-and-customers-amid-lockdown/">
              <img src="@/assets/ventures_africa_logo-min.png" alt="Merchlist featured in Ventures Africa">
          </a>
          <a target="_blank" href="https://techcrunch.com/2019/12/17/nigerias-rensource-raises-20m-to-power-african-markets-by-solar/">
              <img src="@/assets/tech_crunch_logo-min.png" alt="Rensource featured in Tech Crunch" class="tech-crunch">
          </a>
        </div>
      </section>
    </div>
    <div class="footer__newsletter">
      <h4>TradeSpaces</h4>
      <p>Sign up to our newsletter to learn about trade in Africa.</p>
      <mailchimp-subscribe
        url="#"
        user-id="#"
        list-id="#"
        @error="onError"
        @success="onSuccess"
      >
        <template v-slot="{ subscribe, setEmail, error, success, loading }">
          <form @submit.prevent="subscribe">
            <div class="email--inner">
              <input type="email" @input="setEmail($event.target.value)" class="email__input" />
              <button type="submit" class="s-button">Submit</button>
            </div>
            <div v-if="error">{{ error }}</div>
            <div v-if="success">Yay!</div>
            <div v-if="loading">Loading…</div>
          </form>
        </template>
      </mailchimp-subscribe>
    </div>
    <div class="footer__contact">
      <h4 class="footer-contact__header">Contact:</h4>
      <a target="_blank" :href="`mailto:info@spaces.io`" class="footer-contact__email">info@spaces.io</a>
      <a href="tel:+234-901-474-5515" class="footer-contact__mobile">+234 901 474 5515</a>
      <a class="app-link">
        <span>Download App</span>
        <i class="fas fa-external-link-square-alt"></i>
      </a>
    </div>
  </footer>
</template>

<script>
import MailchimpSubscribe from 'vue-mailchimp-subscribe';

export default {
  name: 'el-footer',
  components: {
    MailchimpSubscribe,
  },
};
</script>

<style scoped>
.footer-bg {
  width: 100%;
  background: var(--primaryFour);
}
.s-button {
  box-shadow: 0px 1px 3px rgba(44, 39, 56, 0.08), 0px 1px 3px rgba(44, 39, 56, 0.08);
  width: 12rem;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
  height: 4rem;
  background: var(--primaryOne);
  display: block;
}
.email--inner {
  display: flex;
  align-items: center;
}
.email__input {
  height: 4rem;
  border: 0.4px solid var(--primaryFive);
  border-top-left-radius: 6px;
  border-bottom-left-radius: 6px;
  box-shadow: 0px 1px 1px rgba(44, 39, 56, 0.08), 0px 1px 3px rgba(44, 39, 56, 0.08);
  width: 100%;
  outline: var(--primaryTwo);
}
section {
  margin-top: 1rem;
}
.footer {
  padding: 3rem 6% 2rem;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  background: var(--typeOne);
}
a {
  display: block;
}
a:hover {
  color: var(--primaryOne);
}
.footer-contact__header {
  margin-bottom: 1rem;
}
.footer__press {
  text-align: left;
}
.footer__press {
  width: 30%;
}
.footer__media {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 21rem;
  margin-top: 1rem;
}
.footer__media img {
  width: 10rem;
}
.footer__contact {
  text-align: left;
  width: 20%;
}
.footer-press__spaces-logo {
  width: 22rem;
  margin-top: -10px;
  margin-left: -10px;
}
.footer__newsletter p {
  margin: 1rem 0;
}
.footer__newsletter {
  text-align: left;
}
.footer-contact__email, .footer-contact__mobile, .app-link {
  margin-top: 1rem;
}
h2, h3, h4, p, a {
  color: var(--semanticOne);
}
h2 {
  margin-bottom: 2rem;
}
a {
  font-size: 1.8rem;
}
.app-link .fas {
    padding-left: 0.5rem;
}
@media screen and (max-width: 767px) {
  .footer {
    flex-direction: column;
    padding-bottom: 4rem;
  }
  .footer__press, .footer__newsletter, .footer__contact {
    max-width: 30rem;
    margin-left: 0;
    width: auto;
    margin-top: 1.2rem;
  }
  .footer-press__spaces-logo {
    width: 14rem;
  }
  a {
    font-size: 1.5rem;
    font-weight: 400;
  }
}
</style>

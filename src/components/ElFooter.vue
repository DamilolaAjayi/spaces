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
      <h4>Newsletter</h4>
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
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="external-link-square-alt" class="svg-inline--fa fa-external-link-square-alt fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 80v352c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V80c0-26.51 21.49-48 48-48h352c26.51 0 48 21.49 48 48zm-88 16H248.029c-21.313 0-32.08 25.861-16.971 40.971l31.984 31.987L67.515 364.485c-4.686 4.686-4.686 12.284 0 16.971l31.029 31.029c4.687 4.686 12.285 4.686 16.971 0l195.526-195.526 31.988 31.991C358.058 263.977 384 253.425 384 231.979V120c0-13.255-10.745-24-24-24z"></path></svg>      </a>
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
  methods: {
    onError() {

    },
    onSuccess() {

    },
  }
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
  margin-left: -5px;
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
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
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
  width: 11rem;
  margin-top: 1rem;
}
.footer__media img {
  width: 5rem;
  opacity: 0.8;
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
.app-link {
  display: flex;
  align-items: center;
}
.app-link svg {
    padding-left: 0.5rem;
    width: 15.75px;
    height: 18px;
    box-sizing: content-box;
}
@media screen and (max-width: 767px) {
  .footer {
    flex-direction: column;
  }
  .footer__press, .footer__newsletter, .footer__contact {
    max-width: 30rem;
    margin-left: 0;
    width: auto;
    margin: 1.2rem 0;
  }
  .footer-press__spaces-logo {
    width: 14rem;
  }
  a {
    font-size: 1.5rem;
    font-weight: 400;
  }
  .app-link svg {
      width: 12.75px;
      height: 1.5rem;
  }
}
</style>

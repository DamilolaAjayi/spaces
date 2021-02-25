<template>
    <div>
        <div class="logo">
          <img src="https://ik.imagekit.io/7dkc9ii1v1r/spaces_logo-min_ktkdm48hD.png" alt="Spaces Logo" />
        </div>
        <div class="download-app-modal__header">
            <h3>
                Welcome aboard!
            </h3>
            <p>Ready to manage and grow your business?</p>
        </div>
        <div class="app-link__block">
            <a class="app-link web-app-link" target="_blank" href="https://spaceso2o.com/">
            <span>Visit web app</span>
                <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="external-link-square-alt" class="svg-inline--fa fa-external-link-square-alt fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 80v352c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V80c0-26.51 21.49-48 48-48h352c26.51 0 48 21.49 48 48zm-88 16H248.029c-21.313 0-32.08 25.861-16.971 40.971l31.984 31.987L67.515 364.485c-4.686 4.686-4.686 12.284 0 16.971l31.029 31.029c4.687 4.686 12.285 4.686 16.971 0l195.526-195.526 31.988 31.991C358.058 263.977 384 253.425 384 231.979V120c0-13.255-10.745-24-24-24z"></path></svg>      </a>
            <a class="app-link" target="_blank" href="https://play.google.com/store/apps/details?id=com.spaceso2o.superapp&hl=en&gl=US">
                <span>Download on Google Play</span>
                <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="external-link-square-alt" class="svg-inline--fa fa-external-link-square-alt fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 80v352c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V80c0-26.51 21.49-48 48-48h352c26.51 0 48 21.49 48 48zm-88 16H248.029c-21.313 0-32.08 25.861-16.971 40.971l31.984 31.987L67.515 364.485c-4.686 4.686-4.686 12.284 0 16.971l31.029 31.029c4.687 4.686 12.285 4.686 16.971 0l195.526-195.526 31.988 31.991C358.058 263.977 384 253.425 384 231.979V120c0-13.255-10.745-24-24-24z"></path></svg>      </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'download-spaces-app',
};
</script>

<style scoped>
.logo {
    padding-top: 2rem;
    text-align: center;
    background: var(--neutralTwo);
    min-height: 5.5rem;
    border-bottom: 0.1px solid var(--semanticTwo);
    border-radius: 6px 6px 0 0;
}
img {
    width: 15rem;
    text-align: center;
}
.download-app-modal__header {
    padding: 2rem 0 4rem;
    text-align: center;
}
.download-app-modal__header h3 {
    margin-bottom: 1rem;
    color: var(--typeOne);
}
.app-link {
    margin-bottom: 0.5rem;
    display: inline-flex;
    align-items: center;
    font-weight: 300;
    height: 4rem;
    color: var(--typeOne);
}
.web-app-link {
    flex: 1;
}
.app-link svg {
    width: 12.75px;
    height: 1.5rem;
    padding-left: 0.5rem;
    box-sizing: content-box;
}
.app-link__block {
    display: flex;
    justify-content: space-between;
    padding: 0 1.5rem;
    border-radius: 0 0 6px 6px;
    background: var(--neutralTwo);
    border-top: 0.1px solid var(--semanticTwo);
}
@media screen and (min-width: 768px) {
    .app-link svg {
        width: 15.75px;
        height: 18px;
    }
    .app-link__block {
        padding: 0 3rem;
    }
}
@media screen and (max-width: 330px) {
    .download-app-modal__header p, .app-link  {
        font-size: 1.2rem;
    }
}
</style>
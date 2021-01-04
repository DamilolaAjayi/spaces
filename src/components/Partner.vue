<template>
    <div id="partner" class="partner">
        <div class="partner__textbox">
            <h3>
                Partner With Us
            </h3>
            <p>
                Got a product that will benefit small businesses? Drop us an email and we will reach out.
            </p>
            <a target="_blank" :href="`mailto:info@spaces.io`" class="contact">info@spaces.io</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'partner',
};
</script>

<style lang="scss" scoped>
    .partner {
        min-height: 50vh;
        border-bottom: 0.1rem solid #f2f2f2;
        display: flex;
        padding: 6rem 3rem;
        max-width: 1200px;
        margin: 0 auto;
        &__textbox {
            margin: 0 auto;
            align-self: center;
            text-align: center;
            @media screen and (max-width: 600px) {
                text-align: left;
                align-self: left;
                max-width: 40rem;
                margin: 0;
            }
            h3 {
                font-size: 4rem;
                font-weight: bold;
                text-align: center;
                letter-spacing: 1.2px;
                @media screen and (max-width: 768px) {
                    font-size: 2rem;
                    text-align: left;
                }
            }
            p {
                padding: 3rem 0;
                text-align: left;
                letter-spacing: 0.15rem;
                @media screen and (max-width: 768px) {
                    font-size: 1.6rem;
                }
            }
            a:hover {
                color:#1F2138;
            }
        }
    }
    .contact {
        font-weight: bold;
        font-size: 2rem;
        letter-spacing: -0.05rem;
    }
</style>
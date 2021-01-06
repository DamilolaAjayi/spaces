<template>
    <div id="partner" class="partner">
        <div class="partner__textbox">
            <h2>
                Partner With Us
            </h2>
            <p>
                Got a product that is of benefit to small businesses? Drop us an email and we will reach out.
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
                margin: 0;
            }
            @media screen and (max-width: 768px) {
                text-align: left;
                max-width: 40rem;
            }
            h2 {
                font-size: 4rem;
                font-weight: 600;
                text-align: center;
                @media screen and (max-width: 768px) {
                    font-size: 2rem;
                    text-align: left;
                }
            }
            p {
                padding: 3rem 0;
                text-align: left;
                @media screen and (max-width: 768px) {
                    font-size: 1.6rem;
                }
            }
        }
    }
    .contact {
        font-weight: 600;
        font-size: 2rem;
    }
</style>
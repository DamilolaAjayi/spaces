<template>
    <div id="partner" class="partner">
        <div class="partner__textbox">
            <h3>
                Partner With Us
            </h3>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus, reprehenderit! Ea impedit sit laboriosam quaerat molestiae alias minus magnam eligendi natus, voluptatum, ducimus voluptatibus dolorem unde veniam repellendus, fugit dicta!
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
        background: #1F2138;
        height: 70vh;
        display: flex;
        padding: 6rem 0;
        &__textbox {
            max-width: 60rem;
            margin: 0 auto;
            color: #fff;
            align-self: center;
            text-align: center;
            h3 {
                font-size: 4rem;
                font-weight: bold;
                text-align: center;
            }
            p {
                padding: 3rem 0;
                text-align: left;
                letter-spacing: 0.15rem;
            }
        }
    }
    .contact {
        font-weight: bold;
        font-size: 2rem;
        letter-spacing: -0.05rem;
    }
</style>
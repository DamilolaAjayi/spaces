<template>
    <div class="profile">
        <h2 class="profile--text">
            We have an unparalleled understanding of the <span>informal sector</span>:   
        </h2>
        <div class="profile--highlights">
            <div class="profile--highlights__list">
                <img src="@/assets/store-alt-solid.svg" alt="">
                <p>50,000+ active merchants on SpacesO2O.</p>
            </div>
            <div class="profile--highlights__list">
                <img src="@/assets/network-wired-solid.svg" alt="">
                <p>5,000 agents across Nigeria.</p>
            </div>
            <div class="profile--highlights__list">
                <img src="@/assets/sellsy-brands.svg" alt="">
                <p>N9.5 billion on recorded sales.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'vision',
};
</script>

<style lang="scss" scoped>
    .profile {
        min-height: 70vh;
        padding: 10rem 8rem 1rem;
        border-bottom: 0.1rem solid #f2f2f2;
        max-width: 1200px;
        margin: 0 auto;
        @media screen and (max-width: 992px) {
            padding: 10rem 5rem;
        }
        @media screen and (max-width: 768px) {
            padding: 4rem 2rem;
        }
        &--text {
            max-width: 85rem;
            line-height: 125%;
            font-weight: 400;
            font-size: 4rem;
            padding-bottom: 4rem;
            @media screen and (max-width: 768px) {
                font-size: 2.4rem;
            }
            span {
                border-bottom: 1.5px solid #000;
            }
        }
        &--highlights {
            padding: 8rem 0 3rem;
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            @media screen and (max-width: 768px) {
                flex-direction: column;
                align-items: flex-start;
                padding: 4rem 0;
            }
            &__list {
                padding-top: 2rem;
                display: flex;
                align-items: center;
                @media screen and (max-width: 768px) {
                    font-size: 1.2rem;
                }
                img {
                    margin-right: 0.7rem;
                }
            }
            img {
                width: 36px;
            }
        }
    }
</style>
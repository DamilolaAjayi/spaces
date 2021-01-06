<template>
    <div class="profile">
        <h2 class="profile--text">
            We have an unparalleled understanding of the 
            <a target="_blank" href="https://www.boi.ng/wp-content/uploads/2018/05/BOI-Working-Paper-Series-No2_Economic-Development-through-the-Nigerian-Informal-Sector-A-BOI-perspective.pdf">
                <span>informal sector</span>
            </a>:   
        </h2>
        <div class="profile--highlights">
            <div class="profile--highlights__list">
                <img src="@/assets/store-alt-solid.svg" alt="">
                <p><b>50,000+</b> active merchants on SpacesO2O</p>
            </div>
            <div class="profile--highlights__list">
                <img src="@/assets/network-wired-solid.svg" alt="">
                <p><b>5,000</b> agents across Nigeria</p>
            </div>
            <div class="profile--highlights__list">
                <img src="@/assets/sellsy-brands.svg" alt="">
                <p><b>$1.4 billion</b> in recorded sales</p>
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
        padding: 10rem 15rem 3rem;
        border-bottom: 0.1rem solid #f2f2f2;
        max-width: 1440px;
        margin: 0 auto;
        @media screen and (max-width: 992px) {
            padding: 10rem 5rem;
        }
        @media screen and (max-width: 768px) {
            padding: 4rem 3rem;
        }
        &--text {
            max-width: 85rem;
            line-height: 125%;
            font-weight: 600;
            font-size: 4rem;
            padding-bottom: 4rem;
            @media screen and (max-width: 768px) {
                font-size: 2rem;
                padding-bottom: 1rem;
            }
            span {
                font-weight: 600;
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
                    filter: invert(62%) sepia(57%) saturate(4527%) hue-rotate(180deg) brightness(103%) contrast(101%);
                }
            }
            img {
                width: 36px;
            }
        }
    }
</style>
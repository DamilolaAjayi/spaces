<template>
    <div class="hero">
        <div class="wrapper">
            <div class="section">
                <div class="spaces--brief">
                    <img src="@/assets/spaces_logo_lg.png" alt="Large Spaces logo">
                    <h2 class="hero--text">
                        Building intelligent systems to enhance African trade.
                        <span>Spaces</span> is the backbone for indigenous commerce in Africa.
                    </h2>
                </div>
                <div class="spaces-app">
                    <img src="@/assets/blank-screen-phone-template.png" alt="blank phone screen" class="app-template">
                    <img src="@/assets/Dashboard_Merchant.png" alt="spaces app" class="app">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
};
</script>

<style lang="scss" scoped>
    .wrapper, .section {
        width: 100%;
        height: 100%;
        max-width: 1200px;
        margin: 0 auto;
    }
    .section {
        display: flex;
    }
    .hero {
        height: 85vh;
        padding: 2rem 15rem 0;
        @media screen and (max-width: 1100px) {
            padding: 2rem 4rem 0;
        }
        border-bottom: 0.1rem solid #f2f2f2;
        &--text {
            max-width: 54rem;
            font-weight: 400;
            padding: 3rem 0;
            line-height: 30px;
            span {
                color: #1F2138;
                font-weight: 400;
            }
        }
    }
    .spaces {
        &--brief {
            align-self: center;
            img {
                max-width: 160px;
                @media screen and (max-width: 768px) {
                    max-width: 100px;
                }
            }
        }
        &-app {
            margin-left: 50px;
            position: relative;
            width: 45rem;
            height: 50rem;
            animation: floater 5s linear infinite alternate;
            @media screen and (max-width: 768px) {
                display: none;
            }
        }
    }
    .app {
        width: 19.6rem;
        height: 40.5rem;
        position: absolute;
        top: 6.5%;
        left: 32%;
        @media screen and (max-width: 1200px) {
            left: 33%;
        }
        &-template {
            position: absolute;
            left: 29%;
            height: 46.5rem;
            width: 22rem;
            filter: drop-shadow(0 0 0.5rem #808080);
        }
    }
    @keyframes floater {
        0%  {left:0px; top:0px;}
        50%  {left:0px; top:50px;}
        100% {left:0px; top:0px;}
    }
</style>
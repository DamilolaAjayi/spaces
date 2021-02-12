<template>
    <div class="hero">
        <div class="wrapper">
            <div class="section">
                <div class="spaces--brief">
                    <img src="@/assets/spaces_logo_lg-min.png" alt="Large Spaces logo">
                    <div class="hero--text">
                        <h2>Building Intelligent Systems to Enhance African Trade.</h2>
                        <h3>
                            <span>Spaces</span> is the backbone for informal trade in Africa.
                        </h3>
                    </div>
                </div>
                <div class="spaces-app">
                    <div class="spaces-app-box">
                        <img src="@/assets/android-phone-template-min.png" alt="blank phone screen" class="app-template">
                        <img src="@/assets/spaces-app.png" alt="spaces app" class="app">
                    </div>
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
        @media screen and (max-width: 960px) {
            flex-direction: column;
            margin: 5rem auto 0;
        }
    }
    .hero {
        height: 85vh;
        max-height: 800px;
        padding: 2rem 15rem 0;
        @media screen and (max-width: 1100px) {
            padding: 2rem 4rem 0;
            height: auto;
            max-height: none;      
        }
        border-bottom: 0.1rem solid #f2f2f2;
        &--text {
            max-width: 65rem;
            padding: 3rem 0;
            line-height: 30px;
            h2 {
                font-size: 2.2rem;
                font-weight: 500;
                line-height: 1.4;
            }
            h3 {
                font-size: 1.8rem;
                font-weight: 400;
                opacity: 0.9;
                line-height: 1.8;
                @media screen and (max-width: 768px) {
                    line-height: 1.2;
                    margin-top: 0.5rem;
                }
            }
            @media screen and (max-width: 960px) {
                font-weight: 500;
                font-size: 2rem;
            }
        }
    }
    .spaces {
        &--brief {
            align-self: center;
                @media screen and (max-width: 960px) {
                    padding: 4rem 0 1rem;
                }
            img {
                max-width: 160px;
                @media screen and (max-width: 768px) {
                    max-width: 100px;
                }
            }
        }
        &-app {
            &-box {
                margin-left: 50px;
                position: relative;
                width: 45rem;
                height: 50rem;
                animation: floater 5s linear infinite alternate;
                @media screen and (max-width: 960px) {
                    margin-left: 0;
                    width: auto;
                }
            }
        }
    }
    .app {
        width: 19.6rem;
        height: 40.5rem;
        position: absolute;
        top: 6.5%;
        left: 32%;
        filter: drop-shadow(3px 3px 0.5rem #000000);
        @media screen and (max-width: 1200px) {
            left: 32%;
        }
        @media screen and (max-width: 960px) {
            left: 49.8%;
            margin: 0 auto;
            -webkit-transform: translateX(-50%);
            transform: translateX(-50%)
        }
        &-template {
            position: absolute;
            left: 30%;
            height: 46.5rem;
            width: 21.5rem;
            filter: invert(0%) sepia(2%) saturate(7%) hue-rotate(311deg) brightness(97%) contrast(102%);
            // filter: drop-shadow(0 0 0.5rem #808080);
            @media screen and (max-width: 960px) {
                left: 50%;
                margin: 0 auto;
                -webkit-transform: translateX(-50%);
                transform: translateX(-50%)
            }
        }
    }
    @keyframes floater {
        0%  {top:0px;}
        50%  {top:50px;}
        100% {top:0px;}
    }
</style>
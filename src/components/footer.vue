<template>
    <div class="container" id="footer">
        <div class="wrapper">
            <img src="@/assets/spaces_logo-min.png" alt="spaces logo">
            <div class="spaces--info">
                <div>
                    <a target="_blank" href="https://www.linkedin.com/company/spaceso2o/">
                        <img src="@/assets/linkedin-logo.svg" alt="LinkedIn logo">
                        <span>Connect with us</span>
                    </a>
                </div>
                <div>
                    <a target="_blank" href="https://play.google.com/store/apps/details?id=com.spaceso2o.superapp&hl=en&gl=US" style="margin-left: 0.2rem;">
                        <img src="@/assets/google_play_icon.svg" alt="Google Play Icon">
                        <span>Link to Spaces App</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterElement',
};
</script>

<style lang="scss" scoped>
    .container {
        padding: 6rem 10rem;
        border-top: 0.1rem solid #f2f2f2;
        @media screen and (max-width: 992px) {
            padding: 4rem 3rem;
        }
        img {
            max-height: 48px;
            @media screen and (max-width: 992px) {
                max-height: 4rem;
            }
            @media screen and (max-width: 600px) {
                max-height: 3rem;
            }
        }
    }
    .wrapper {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        @media screen and (max-width: 600px) {
            flex-direction: column;
            align-items: flex-start;
        }
    }
    .spaces--info {
        display: flex;
        float: right;
        align-items: baseline;
        @media screen and (max-width: 600px) {
            flex-direction: column;
            margin-top: 2rem;
        }
        a {
            align-items: center;
            display: flex;
            font-size: 1.5rem;
            padding-left: 1.6rem;
            @media screen and (max-width: 768px) {
                font-size: 1.2rem;
            }
            @media screen and (max-width: 600px) {
                padding-left: 0;
            }
            span {
                padding-left: 0.5rem;
            }
        }
        img {
            width: 2.4rem;
            height: 2.4rem;
        }
    }
</style>
<template>
    <div class="container" id="footer">
        <div class="wrapper">
            <img src="@/assets/spaces_logo.png" alt="spaces logo">
            <div class="spaces--info">
                <div>
                    <img src="@/assets/linkedin-logo.svg" alt="LinkedIn logo">
                    <p style="margin-left: 0.2rem;">Connect with us</p>
                </div>
                <div>
                    <img src="@/assets/google_play_icon.svg" alt="Google Play Icon">
                    <p style="margin-left: 0.2rem;">Link to Spaces App</p>
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
        img {
            max-height: 48px;
        }
    }
    .wrapper {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .spaces--info {
        display: flex;
        float: right;
        align-items: baseline;
        div {
            align-items: center;
            display: flex;
            padding-left: 1.6rem;
        }
        p {
            font-size: 1.5rem;
        }
        img {
            width: 2.4rem;
            height: 2.4rem;
        }
    }
</style>
<template>
    <div class="investors">
        <!-- <div class="investors--block">
            <h2 class="investors--header">Our Backers</h2>
            <div class="investor">
                <img src="@/assets/rensource_logo.png" alt="Rensource Energy">
            </div>
        </div> -->
        <div class="investors--block">
            <h2>In the News</h2>
            <div class="media">
                <a target="_blank" href="http://venturesafrica.com/rensource-launches-platform-to-connect-retailers-and-customers-amid-lockdown/">
                    <img src="@/assets/ventures_africa_logo.png" alt="Merchlist featured in Ventures Africa">
                </a>
                <a target="_blank" href="https://techcrunch.com/2019/12/17/nigerias-rensource-raises-20m-to-power-african-markets-by-solar/">
                    <img src="@/assets/tech_crunch_logo.png" alt="Rensource featured in Tech Crunch">
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'investors',
};
</script>

<style lang="scss" scoped>
    .investors{
        padding: 8rem 15rem;
        border-bottom: 0.1rem solid #f2f2f2;
        display: flex;
        justify-content: space-around;
        max-width: 1200px;
        margin: 0 auto;
        @media screen and (max-width: 600px) {
            flex-direction: column;
        }
        @media screen and (max-width: 1100px) {
            padding: 8rem 3rem;
        }
        &--block {
            text-align: center;
            h2 {
                font-weight: 600;
                font-size: 4rem;
                @media screen and (max-width: 768px) {
                    font-size: 2rem;
                }
            }
            img {
                filter: grayscale(100%);
                opacity: 0.8;
                -webkit-transition: all 200ms ease;
                -webkit-filter: grayscale(100%);
                transition: all 200ms ease;
                @media screen and (max-width: 768px) {
                    max-height: 4rem;
                }
            }
        }
    }
    .media {
        display: flex;
        justify-content: space-between;
        margin-top: 2rem;
        width: 35rem;
        @media screen and (max-width: 900px) {
            margin: 2rem auto 0;
        }
        @media screen and (max-width: 768px)  {
            width: 24rem;
        }
        img {
            max-height: 10rem;
            @media screen and (max-width: 768px) {
                max-height: 6rem;
            }
        }
    }
    .investor {
        margin: 3.5rem 0;
    }
</style>
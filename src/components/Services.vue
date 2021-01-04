<template>
    <div class="about" id="about">
        <h2 class="about--text">
            Businesses exist to make money. We connect businesses to money faster and profitably by:
        </h2>
        <div class="services">
            <div class="offerings">
                <img src="@/assets/increasing-demand.svg" alt="">
                <div class="block">
                    <h3>Increasing Demand</h3>
                   <p>through our wholesale and retail ordering platforms that connect sellers to buyers.</p>
                </div>
            </div>
            <div class="offerings">
                <img src="@/assets/cash-flow.svg" alt="">
                <div class="block">
                    <h3>Improving Cashflow</h3>
                    <p>with credit facilities that ensure business needs are met.</p>
                </div>
            </div>
            <div class="offerings">
                <img src="@/assets/chain.svg" alt="">
                <div class="block">
                    <h3>Strengthening Supply Chain</h3>
                    <p>streamlining the flow of goods from Distributors and Wholesalers to merchants.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'services',
};
</script>

<style lang="scss" scoped>
    .about {
        min-height: 100vh;
        padding: 10rem 15rem;
        border-bottom: 0.1rem solid #f2f2f2;
        max-width: 1200px;
        margin: 0 auto;
        @media screen and (max-width: 1100px) {
            padding: 8rem 5rem;
        }
        &--text {
            max-width: 85rem;
            line-height: 125%;
            font-weight: 400;
            font-size: 4rem;
            margin-bottom: 4rem;
            @media screen and (max-width: 768px) {
                font-size: 2.4rem;
            }
        }
    }
    .services {
        display: flex;
        justify-content: space-between;
        padding-top: 4rem;
        @media screen and (max-width: 768px) {
            flex-direction: column;
            align-items: center;
        }
    }
    .offerings {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 30%;
        @media screen and (max-width: 768px){
            width: 430px;
        }
        @media screen and (max-width: 450px){
            width: auto;
        }
        .block {
            margin-top: 5.8rem;
            @media screen and (max-width: 768px){
                margin: 1rem 0 6rem;
            }
        }
        img {
            width: 150px;
            height: 150px;
            opacity: 0.8;
        }
        h3 {
            font-weight: bold;
            align-self: flex-start;
            margin-bottom: 1rem;
            padding-top: 2rem;
        }
        p {
            align-self: flex-start;
        }
    }
</style>
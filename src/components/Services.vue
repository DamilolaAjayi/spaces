<template>
    <div class="about" id="about">
        <h2 class="about--text">
            We help our merchants make money by:
        </h2>
        <div class="services">
            <div class="offerings">
                <img src="@/assets/increasing-demand.svg" alt="">
                <div class="block">
                    <h3>Increasing Demand</h3>
                   <p>Access to our robust e-commerce platform for wholesale and retail.</p>
                </div>
            </div>
            <div class="offerings">
                <img src="@/assets/cash-flow.svg" alt="">
                <div class="block">
                    <h3>Improving Cashflow</h3>
                    <p>Credit facilities that ensure business needs are met.</p>
                </div>
            </div>
            <div class="offerings">
                <img src="@/assets/supply-chain.svg" alt="">
                <div class="block">
                    <h3>Strengthening Supply Chain</h3>
                    <p>Streamlining the flow of goods from distributors and wholesalers to merchants.</p>
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
        padding: 10rem 15rem;
        border-bottom: 0.1rem solid #f2f2f2;
        max-width: 1440px;
        margin: 0 auto;
        @media screen and (max-width: 1100px) {
            padding: 8rem 3rem;
        }
        &--text {
            max-width: 85rem;
            line-height: 125%;
            font-weight: 600;
            font-size: 4rem;
            margin-bottom: 4rem;
            @media screen and (max-width: 768px) {
                font-size: 2rem;
                margin-bottom: 0;
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
            margin-top: 1.5rem;
            @media screen and (max-width: 768px){
                margin: 1rem 0 6rem;
            }
        }
        img {
            width: 250px;
            height: 250px;
            opacity: 0.8;
            margin-left: -20px;
            @media screen and (max-width: 600px){
                margin-left: 0;
            }
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
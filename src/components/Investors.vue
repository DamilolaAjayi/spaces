<template>
    <div class="investors">
        <div class="investors--block">
            <h2>Our Backers</h2>
        </div>
        <div class="investors--block">
            <h2>In the News</h2>
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
        display: flex;
        &--block {
            text-align: center;
            align-self: center;
            h2 {
                font-weight: bold;
            }
        }
    }
</style>
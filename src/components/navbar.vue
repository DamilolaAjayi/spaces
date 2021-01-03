<template>
    <div class="nav">
        <a href="#footer" class="nav-link">About</a>
        <a href="#partner" class="nav-link">Partner</a>
    </div>
</template>

<script>
export default {
    name: 'navbar',
};
</script>

<style lang="scss" scoped>
    .nav {
        padding: 4.8rem 12rem 0;
        display: flex;
        justify-content: flex-end;
        color: #1F2138;
        &-link {
            padding: 2rem;    
            position: relative;
            display: inline-block;
            vertical-align: top;
            text-decoration: none;
            text-align: left;
            font-size: 1.6rem;
            line-height: 2.4rem;
            font-weight: 500;
        }
    }
</style>
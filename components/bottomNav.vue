<template>
    <div class="menu">
        <img src="/img/left.png">
        <img src="/img/home.png">
        <img src="/img/personal.png">
    </div>
</template>
<style scoped lang="scss">
    .menu {
        position: fixed;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 50px;
        background-color: #B39872;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        >img {
            width: 25px;
        }
    }
</style>
<script>
export default ({
    data () {
        return {
            
        }
    },
    methods: {
    },
})
</script>
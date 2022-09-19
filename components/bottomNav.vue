<template>
    <div class="menu">
        <img src="/img/left.png" @click="$router.go(-1)">
        <img src="/img/home.png" @click="$router.push('/menu')">
        <img src="/img/personal.png" @click="$router.push('/userData')">
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
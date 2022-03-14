<template>
    <div class="menu">
        <img src="/img/menu.svg" @click="showMenu = !showMenu">
        <transition>
            <div v-show="showMenu" class="menu_list">
                <img src="/img/close.svg" @click="showMenu = !showMenu">
                <div v-for="(item, id) in menuList" :key="id + 'menu'">
                    <div>
                        <a @click="$router.push(`${item.link}`)">{{ item.tag }}</a>
                    </div>
                </div>
            </div>
        </transition>
    </div>
</template>
<style scoped lang="scss">
    .menu {
        display: flex;
        justify-content: flex-end;
        .menu_list {
            width: 100%;
            height: 100vh;
            background-color: #B39872;
            position: fixed;
            top: 0;
            left: 0;
            >img {
                position: absolute;
                right: 20px;
                top: 20px;
            }
        }
    }
    .v-enter, .v-leave-to {
        opacity: 0;
        transform: translateX(100vw);
    }
    .v-leave, .v-enter-to {
        opacity: 1;
    }
    .v-enter-active {
        transition: all 0.3s ease;
    }
    .v-leave-active {
        transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
    }
</style>
<script>
export default ({
    data () {
        return {
            showMenu: false,
            menuList: [
                { tag: '公司簡介', link: '/information' },
                { tag: '預約服務', link: '/information' },
                { tag: '聯絡資訊', link: '/contact' },
                { tag: '公司簡介', link: '/information' },
                { tag: '公司簡介', link: '/information' },
            ]
        }
    },
    methods: {
    },
})
</script>

http://localhost:52992/information
http://localhost:52992/information
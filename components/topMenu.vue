<template>
    <div class="menu">
        <img src="/img/menu.svg" @click="showMenu = !showMenu">
        <transition>
            <div v-show="showMenu" class="menu_list">
                <img src="/img/close.svg" @click="showMenu = !showMenu">
                <div class="list">
                    <div v-for="(item, id) in menuList" :key="id + 'menu'" class="list_inner">
                        <a @click="$router.push(`${item.link}`)" class="list_content">{{ item.tag }}</a>
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
            display: flex;
            justify-content: center;
            align-items: center;
            >img {
                position: absolute;
                right: 20px;
                top: 20px;
            }
            .list {
                display: flex;
                flex-direction: column;
                .list_inner {
                    margin-bottom: 20px;
                    .list_content {
                        font-weight: bold;
                        color: #ffffff;
                        font-size: 20px;
                    }
                }
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
                { tag: '會員資料', link: '/userData' },
                { tag: '公司簡介', link: '/contact' },
                { tag: '最新消息', link: '/' },
                { tag: '價目表', link: '/information' },
                { tag: '聯絡資訊', link: '/contact' },
            ]
        }
    },
    methods: {
    },
})
</script>

http://localhost:52992/information
http://localhost:52992/information
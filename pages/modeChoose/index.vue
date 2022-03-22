<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">已登記車輛</div>
        </div>
        <div class="content_box">
            <div class="signInBox" v-for="(item, id) in form" :key="id + 'form'">
                <b-form-input
                    :id="`input-${id}`"
                    v-model="item.content"
                    :name="`input-${id}`"
                    :placeholder="item.placeholder"
                    disabled="true"
                ></b-form-input>
            </div>
            <div class="sign_box">
                <b-btn @click="$router.push('/changePassword')">確認</b-btn>
            </div>
        </div>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/userData/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            form: {
                name: {
                    label: '姓名', placeholder: '車牌號碼', content: '車牌號碼', inputName: '帳號'
                },
                birth: {
                    label: '生日', placeholder: '推薦戶', content: '推薦戶', inputName: '生日'
                },
            },
        }
    },
    methods: {
        
    },
})
</script>

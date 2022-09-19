<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">登入</div>
        </div>
        <div class="content_box">
            <div class="signInBox" v-for="(item, id) in form" :key="id + 'form'">
                <div class="input_title">{{ item.inputName }}</div>
                <b-form-input
                    :id="`input-${id}`"
                    v-model="item.content"
                    :name="`input-${id}`"
                    :placeholder="item.placeholder"
                ></b-form-input>
            </div>
            <div class="sign_box">
                <b-btn>登入</b-btn>
                <div class="signUp_text">
                    <div>還沒有帳號嗎？</div>
                    <a @click="$router.push('/signUp')" class="signUp">註冊</a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/signIn/style.min.css";
</style>
<script>
import axios from '~/plugins/axios'
export default ({
    data () {
        return {
            form: {
                // type 1 => input, type 2 => checkbox, type 2 => link
                account: {
                    label: '帳號', placeholder: '請輸入帳號', content: '', inputName: '帳號'
                },
                password: {
                    label: '密碼', placeholder: '請輸入密碼', content: '', inputName: '密碼'
                }
            },
        }
    },
    methods: {
        
    },
    mounted() {
        console.log('燈')
        axios.post(`/com/webApi/user/login`, {uraccount: "admin", urpassword: "admin1234"}).then((res) => {
            console.log(res)
        }).catch((er) => {
            console.log('沒過')
            console.log(er)
        })
    },
})
</script>

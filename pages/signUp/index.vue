<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">註冊新帳戶</div>
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
                <b-btn>註冊</b-btn>
                <div class="signUp_text">
                    <div>已經有帳號了嗎？</div>
                    <a @click="$router.push('/signIn')" class="signUp">登入</a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/signUp/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            form: {
                // type 1 => input, type 2 => checkbox, type 2 => link
                name: {
                    label: '姓名', placeholder: '請輸入中文姓名', content: '', inputName: '帳號'
                },
                birth: {
                    label: '生日', placeholder: '請輸入西元年/月/日', content: '', inputName: '生日'
                },
                phone: {
                    label: '手機', placeholder: '請輸入手機號碼', content: '', inputName: '手機'
                },
                mail: {
                    label: '信箱', placeholder: '請輸入正確信箱格式', content: '', inputName: '信箱'
                },
                password: {
                    label: '密碼', placeholder: '請輸入至少8位數以上的英文及數字', content: '', inputName: '密碼'
                },
                confirm: {
                    label: '確認密碼', placeholder: '請再次確認密碼', content: '', inputName: '確認密碼'
                },
                address: {
                    label: '地址', placeholder: '請輸入居住地址', content: '', inputName: '地址'
                },
            },
        }
    },
    methods: {
        
    },
})
</script>

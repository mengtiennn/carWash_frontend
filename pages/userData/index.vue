<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">會員資料</div>
        </div>
        <div class="content_box">
            <div class="note">如需修改資料請洽管理員</div>
            <div class="signInBox" v-for="(item, id) in form" :key="id + 'form'">
                <div class="input_title">{{ item.inputName }}</div>
                <b-form-input
                    :id="`input-${id}`"
                    v-model="item.content"
                    :name="`input-${id}`"
                    :placeholder="item.placeholder"
                    disabled="true"
                ></b-form-input>
            </div>
            <div class="sign_box">
                <b-btn @click="$router.push('/changePassword')">變更密碼</b-btn>
            </div>
        </div>
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
                    label: '姓名', placeholder: '請輸入中文姓名', content: 'apiData', inputName: '帳號'
                },
                birth: {
                    label: '生日', placeholder: '請輸入西元年/月/日', content: 'apiData', inputName: '生日'
                },
                phone: {
                    label: '手機', placeholder: '請輸入手機號碼', content: 'apiData', inputName: '手機'
                },
                mail: {
                    label: '信箱', placeholder: '請輸入正確信箱格式', content: 'apiData', inputName: '信箱'
                },
                address: {
                    label: '地址', placeholder: '請輸入居住地址', content: 'apiData', inputName: '地址'
                },
            },
        }
    },
    methods: {
        
    },
})
</script>

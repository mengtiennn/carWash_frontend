<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">修改密碼</div>
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
                ></b-form-input>
            </div>
            <div class="sign_box">
                <b-btn>確認</b-btn>
            </div>
        </div>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/changePassword/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            form: {
                name: {
                    label: '手機號碼', placeholder: '請輸入手機號碼', content: '', inputName: '手機號碼'
                },
                birth: {
                    label: '信箱', placeholder: '請輸入信箱', content: '', inputName: '信箱'
                },
                phone: {
                    label: '變更密碼', placeholder: '請輸入至少8位數以上的英文數字', content: '', inputName: '變更密碼'
                },
                mail: {
                    label: '變更密碼再確認', placeholder: '請輸入至少8位數以上的英文數字', content: '', inputName: '變更密碼再確認'
                },
            },
        }
    },
    methods: {
        
    },
})
</script>

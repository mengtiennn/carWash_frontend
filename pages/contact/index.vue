<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">聯絡我們</div>
        </div>
        <div class="content_text">感謝您的支持與愛護，如果有任何疑問，歡迎使用以下任一方式聯絡我們，或是寄信至XXXXXXX，我們會有專人為您服務。感謝您！</div>
        <div class="contact_box">
            <div class="contact_content">
                <img src="/img/ig.svg">
                <div>abc12345</div>
            </div>
            <div class="contact_content">
                <img src="/img/fb.svg">
                <div>abc12345</div>
            </div>
            <div class="contact_content">
                <img src="/img/line.svg">
                <div>abc12345</div>
            </div>
        </div>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/contact/style.min.css";
</style>
<script>
import bottomNav from "/components/bottomNav.vue"
export default ({
    components: { bottomNav },
    data () {
        return {
            form: {
                name: {
                    label: '車輛號碼', placeholder: '請輸入完整車牌號碼，例：ABC-1234', content: '', inputName: '車牌號碼'
                },
                birth: {
                    label: '推薦代碼', placeholder: '請輸入推薦戶代碼（非必填）', content: '', inputName: '推薦代碼'
                },
            },
        }
    },
    methods: {
        
    },
})
</script>

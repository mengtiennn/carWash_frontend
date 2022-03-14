<template>
    <div class="wrapper">
        <div class="title_box">
            <div class="title_text">新增車輛</div>
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
                <b-btn>確認</b-btn>
            </div>
        </div>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/carAdd/style.min.css";
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

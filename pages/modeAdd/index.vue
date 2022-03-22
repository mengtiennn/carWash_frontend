<template>
    <div class="wrapper">
        <div class="date">2022-03-22</div>
        <div class="select_box">
            <div class="select_title">選擇預約車輛</div>
            <b-form-select v-model="selected_car" :options="options_car"></b-form-select>
        </div>
        <div class="select_box">
            <div class="select_title">選擇預約時段</div>
            <b-form-select v-model="selected_time" :options="options_time"></b-form-select>
        </div>
        <div class="goCheck">確認預約</div>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/carOrder/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            selected_car: null,
            selected_time: null,
            options_car: [
                { value: null, text: '請選擇車輛' },
                { value: 'ABC-1234', text: 'ABC-1234' },
                { value: 'ABC-1234', text: 'ABC-1234' },
                { value: 'ABC-1234', text: 'ABC-1234' },
                { value: 'ABC-1234', text: 'ABC-1234' },
                { value: 'ABC-1234', text: 'ABC-1234' },
            ],
            options_time: [
                { value: null, text: '請選擇時段' },
                { value: '8:00', text: '8:00' },
                { value: '9:00', text: '9:00' },
                { value: '10:00', text: '10:00' },
                { value: '11:00', text: '11:00' },
                { value: '13:00', text: '13:00' },
                { value: '14:00', text: '14:00' },
                { value: '15:00', text: '15:00' },
                { value: '16:00', text: '16:00' },
                { value: '17:00', text: '17:00' },
            ]
        }
    },
    methods: {
        
    },
})
</script>

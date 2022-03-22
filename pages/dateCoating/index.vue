<template>
    <div class="wrapper">
        <div class="resBtn">
            <div class="btnInside" @click="$router.push('/carOrder')">洗車預約</div>
            <div class="btnInside" @click="$router.push('/modeAdd')">鍍膜預約</div>
        </div>
        <client-only>
            <v-date-picker
                :value="null"
                :min-date="new Date()"
                is-expanded
            />
        </client-only>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/dateCoating/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            
        }
    },
    methods: {
        
    },
})
</script>

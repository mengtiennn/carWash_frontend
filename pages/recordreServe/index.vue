<template>
    <div class="wrapper">
        <b-table :items="items" :fields="fields"></b-table>
        <bottomNav/>
    </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/recordBonus/style.min.css";
</style>
<script>
export default ({
    data () {
        return {
            fields: [
                { key: '編號', sortable: false },
                { key: '車牌號碼', sortable: false },
                { key: '日期', sortable: false },
                { key: '時段', sortable: false},
                { key: '類型',  sortable: false},
            ],
            items: [
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
                { '編號': '123', '車牌號碼': 'ABC-1234', '日期': '2021-10-10', '時段': '09:10', '類型': '鍍膜'},
            ]
        }
    },
    methods: {
        
    },
})
</script>

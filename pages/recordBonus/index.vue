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
                { key: '推薦人', sortable: false },
                { key: '日期', sortable: false },
                { key: '金額', sortable: false},
                { key: '類型',  sortable: false},
            ],
            items: [
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
                { '編號': '123', '推薦人': 'test01', '日期': '2021-10-10', '金額': 1000, '類型': '匯款'},
            ]
        }
    },
    methods: {
        
    },
})
</script>

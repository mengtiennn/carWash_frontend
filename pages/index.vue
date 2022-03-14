<template>
  <div class="wrapper">
    <topMenu/>
    <div class="member_info">
      <div class="member_name">{{ memberData.name }}</div>
      <div class="member_num">{{ memberData.num }}</div>
    </div>
    <div class="car_info">
      <div class="inside_info" v-for="(item, id) in infoList" :key="id + 'info'">
        <div class="info_title">{{ item.title }}</div>
        <div class="info_data">{{ item.content }}</div>
      </div>
    </div>
    <div class="service">
      <div class="service_inside" v-for="(item, id) in service" :key="id + 'service'" @click="$router.push(`${item.link}`)">
        <img :src="item.img">
        <div class="service_title">{{ item.title }}</div>
      </div>
    </div>
  </div>
</template>
<style scoped>
    @import "~assets/css/global.min.css";
</style>
<style scoped>
    @import "~assets/css/style.min.css";
</style>
<script>
import topMenu from "/components/topMenu.vue"
export default {
  components: { topMenu },
  data () {
    return {
      infoList: [
        { title: '目前紅利金額', content: 'apiData' },
        { title: '擁有車輛數', content: 'apiData' },
        { title: '最新預約日', content: 'apiData' },
        { title: '目前身份', content: 'apiData' },
      ],
      memberData: { name: 'Member001', num: '234567' },
      service: [
        { title: '會員資料', img: '/img/person.svg', link: '/userData' },
        { title: '車輛登記', img: '/img/car.svg', link: '/carAdd' },
        { title: '查詢車輛', img: '/img/search.svg', link: '/userData' },
        { title: '即時預約', img: '/img/calendar.svg', link: '/userData' },
        { title: '預約記錄', img: '/img/assignment.svg', link: '/userData' },
        { title: '紅利紀錄', img: '/img/money.svg', link: '/userData' },
      ]
    }
  }

}
</script>

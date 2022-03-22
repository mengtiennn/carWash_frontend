<template>
  <div class="wrapper">
    <div class="car_loading" v-if="showImg">
      <img src="/img/carloading.gif">
    </div>
    <div class="car_carousel" v-if="!showImg">
      <client-only>
        <carousel v-bind="options" autoplay>
          <slide>
            <img src="/img/car3.jpeg" style="width: 100%;">
          </slide>
          <slide>
            <img src="/img/car2.jpeg" style="width: 100%;">
          </slide>
          <slide>
            <img src="/img/car4.jpeg" style="width: 100%;">
          </slide>
          <slide>
            <img src="/img/car5.jpeg" style="width: 100%;">
          </slide>
          <slide>
            <img src="/img/car6.jpeg" style="width: 100%;">
          </slide>
        </carousel>
      </client-only>
      <div class="index_title">歡迎蒞臨 XXXXXXX</div>
      <div @click="$router.push('/menu')">進入會員介面</div>
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
      showImg: true,
      options: {
        loop: true,
        perPage: 1,
        paginationEnabled: false
      }
    }
  },
  methods: {
    show () {
      setTimeout(() => {
        this.showImg = false
      }, 3000)
    }
  },
  mounted() {
    this.show()
  },

}
</script>

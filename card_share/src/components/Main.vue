<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide one">Slide 1</div>
      <div class="swiper-slide two">Slide 2</div>
      <div class="swiper-slide three">Slide 3</div>
      <div class="swiper-slide four">
        <p>扫描下方二维码</p>
        <p>获取你的消费总结</p>
      </div>
    </div>

    <div class="swiper-pagination"></div>
    <!-- 滚动条 -->
    <!-- <div class="swiper-scrollbar"></div> -->
  </div>

</template>

<script>
import Swiper from 'swiper'
import dayjs from 'dayjs'
import 'swiper/dist/css/swiper.min.css'

export default {
  components: {

  },
  props: {

  },
  data() {
    return {

    }
  },
  methods: {},
  mounted() {
    let mySwiper = new Swiper('.swiper-container', {
      pagination: {
        el: '.swiper-pagination',
      },
      //垂直滚动
      direction: 'vertical',
    })
  }
}
</script>
<style scoped>
.swiper-container {
    width: 300px;
    height: 500px;
    margin: 20px auto;
}
.one {
    background-color: aqua;
}
.two {
    background-color: blue;
}
.three {
    background-color: gray;
}
.four {
    background-color: cornflowerblue;
}
</style>
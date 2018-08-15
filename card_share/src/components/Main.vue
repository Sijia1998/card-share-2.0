<template>
  <div class="swiper">
    <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
      <!-- slides -->
      <swiper-slide class="table">
        <div class="center">
          <p>学期账单</p>
          <p>点击查看</p>
        </div>
        <img src="" alt="" style="width:30px">
      </swiper-slide>
      <swiper-slide>I'm Slide 2</swiper-slide>
      <swiper-slide>I'm Slide 3</swiper-slide>
      <swiper-slide>I'm Slide 4</swiper-slide>
      <swiper-slide>I'm Slide 5</swiper-slide>
      <swiper-slide>I'm Slide 6</swiper-slide>
      <swiper-slide>I'm Slide 7</swiper-slide>
      <!-- Optional controls -->
      <!-- <div class="swiper-pagination" slot="pagination"></div> -->

    </swiper>
  </div>
</template>

<script>
import axios from 'axios'
import dayjs from 'dayjs'
import 'swiper/dist/css/swiper.css'


export default {
  data() {
    return {
      costTotal: 5800,
      costRes: 66666,
      swiperOption: {
        // some swiper options/callbacks
        // 所有的参数同 swiper 官方 api 参数
        // ...
        direction: 'vertical',
        fade: 'true',
        autoplay: false,
        // speed: 1000,
        height: window.innerHeight,
        width: window.innerWidth
      }
    }
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper
    }
  },
  methods: {
    // getInit() {
    //   let self = this;
    //   let begindate = dayjs().format('2018-03-04');
    //   let enddate = dayjs().format('2018-07-12')
    //   axios.get('http://118.126.110.182:8002/api/getNewData', {
    //     params: {
    //       begindate,
    //       enddate,
    //     },
    //     headers: {
    //       'Content-Type': 'application/x-www-form-urlencoded'
    //     },
    //   })
    //     .then((res) => {
    //       console.log(res);

    //     })
    // }
  },
  mounted() {
    console.log("this is current swiper instance object", this.swiper);
    // this.getInit()
  }
}
</script>
<style scoped>
.center {
    /* text-align: center; */
    background: aqua;
    position: absolute;
    top: 50%;
    left: 50%;
    width: 50%;
    height: 50%;
    -webkit-transform: translateX(-50%) translateY(-50%);
}
</style>
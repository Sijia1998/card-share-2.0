<template>
  <div class="swiper">
    <div>
      <audio src="/static/music.mp3" autoplay="autoplay" loop="loop"></audio>
    </div>
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide class="flex">
        <div class="center">
          <p class="textCenter">学期账单</p>
          <p class="textCenter">点击查看</p>
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>
      <swiper-slide class="flex">
        <div class="center">
          <p>时光总是偷偷流逝</p>
          <p>打开一卡通账单</p>
          <p>看看这一学期是不是</p>
          <p>过的不太一样</p>
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>
      <swiper-slide class="flex">
        <div class="center third">
          <p>总共花费5800元</p>
          <p>旭日苑餐厅得到你的青睐</p>
          <p>总共消费66666元</p>
          <p>解衣宽带终不恼，吃完记得，擦擦嘴</p>
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>
      <swiper-slide class="flex">
        <div class="center">
          <p>光顾图书馆二楼超市10次</p>
          <p>总共消费99元</p>
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>
      <swiper-slide class="flex">
        <div class="center">
          <p>你为 花费了66元</p>
          <p>唯美食与爱不可辜负</p>
          <p>黄焖鸡米饭是你的最爱</p>
          <p>去了10次</p>
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>
      <swiper-slide class="flex">
        <p class="fontSize">扫描下方二维码即可获取你的消费信息</p>
        <div class="center img">
          
        </div>
        <p class="swiper_bottom">智邮普创工作室</p>
      </swiper-slide>

      <!-- Optional controls -->
      <!-- <div class="swiper-pagination" slot="pagination"></div> -->

    </swiper>
  </div>
</template>

<script>
import axios from 'axios'
import dayjs from 'dayjs'


export default {
  data() {
    return {
      costTotal: 5800,
      costRes: 66666,
      swiperOption: {
        // some swiper options/callbacks
        // 所有的参数同 swiper 官方 api 参数
        // ...
        observer: true,
        observeParents: true,
        autoHeight: true,
        direction: 'vertical',
        fade: 'true',
        autoplay: false,
        // speed: 1000,
        height: window.innerHeight,
        width: window.innerWidth,

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

.flex {
    display: flex;
    text-align: center;
}
.swiper_bottom {
    position: absolute;
    bottom: 1rem;
    text-align: center;
    width: 100%;
    font-size: 0.9rem;
}
.center {
    /* background: aqua; */
    font-size: 1.5rem;
    text-align: center;
    margin: auto;
}
.textCenter {
    text-align: center;
}
.third {
    width: 80%;
    text-align: center;
}
.fontSize {
    width: 100%;
    position: absolute;
    text-align: center;
    top: 20%;
    font-size: 1.5rem;
}
</style>
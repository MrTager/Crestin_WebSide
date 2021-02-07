<template>
  <div class="product">
        <!-- <img class="bannerImg" src="../assets/images/product.png"> -->
        <div class="swiper-container">
         <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide><div class="imgBox"><img src="../assets/images/thing_2.png"><p>Smart Plug</p></div></swiper-slide>
            <swiper-slide><div class="imgBox"><img src="../assets/images/thing_1.png"><p>Light Bulb</p></div></swiper-slide>
            <swiper-slide><div class="imgBox"><img src="../assets/images/thing_4.png"><p>Outdoor Plugs</p></div></swiper-slide>
            <swiper-slide><div class="imgBox"><img src="../assets/images/thing_3.png"><p>Light Strip</p></div></swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
         <!-- 如果需要导航按钮 -->
            <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div>
        </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: 'Product',
  components: {
    Swiper,
    SwiperSlide
  },
  directives: {
    swiper: directive
  },
  data () {
    return {
      msg: '',
       swiperOptions: {
          pagination: {
            el: '.swiper-pagination'
          },
          navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev',
          },
          scrollbar: {
            el: '.swiper-scrollbar',
         },
        nextButton: '.swiper-button-next',
        prevButton: '.swiper-button-prev',
        loop: true, // 循环模式选项
        speed:500,
        autoplay : {
            delay:3000
        },
          // Some Swiper option/callback...
        }
    }
   },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted(){
      console.log('Current Swiper instance object', this.swiper)
      this.swiper.slideTo(2, 1000, false)
    },
}
</script>
<style lang="scss" scoped>
.product{
    width: 100%;
    height: 300px;
}
.swiper-container {
        width: 100%;
        height: 100%;
        margin-left: auto;
        margin-right: auto;
}
.swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
}
.imgBox{
    width: 400px;
    height: 250px;
    box-shadow: 0 0 10px 10px rgb(240, 240, 240);
    img{
        width: 200px;
        height: 200px;
    }
    p{
        font-size: 20px;
        color: rgb(31 ,159 ,198);
        font-family: Helvetica, 'Hiragino Sans GB', 'Microsoft Yahei', '微软雅黑', Arial, sans-serif;
    }
}
.swiper-button-prev{
    margin-left: 20%;
}
.swiper-button-next{
    margin-right: 20%;
}
</style>

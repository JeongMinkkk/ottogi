<template>
  <!-- 브랜드배너 슬라이드 -->
  <div class="max-w-7xl mx-auto h-full mb-20">
      <div class="basis-full h-32 border rounded-xl">
        <swiper  class="content_2" :modules="modules" :navigation="{prevEl:'.swiper-button-prev',nextEl:'.swiper-button-next'}">
          <swiper-slide v-for="(e,index) in 3" :key="index">
            <a href="#">
              <img :src="require(`@/assets/images/band-bnr_0${index+1}.png`)" alt="e" class="rounded-xl w-full h-32">
            </a>
            <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';


// import required modules
import { Navigation } from 'swiper';
import { Pagination } from 'swiper';


export default {
  name:"HomeBanner",
  data() {
    return {
      
    }
  },
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation, Pagination]
      };
    }
}
</script>
<style>
 .content_2 .swiper-button-prev {
  background: url(../../assets/images/R_arrow_banner.svg) no-repeat;
  background-size: 50% auto;
  background-position: center;
}
.content_2 .swiper-button-next {
  background: url(../../assets/images/L_arrow_banner.svg) no-repeat;
  background-size: 50% auto;
  background-position: center;
}
.content_2 .swiper-button-prev::after,
.content_2 .swiper-button-next::after {
  display: none;
}
</style>
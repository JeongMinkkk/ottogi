<template>
  <!-- 이런상품 어때요 -->
  <div class="max-w-7xl mx-auto h-full mb-20">
      <h2 class="text-3xl font-bold">이런상품 어때요</h2>
      <swiper :slidesPerView="5" :spaceBetween="10" :freeMode="true" :scrollbar="{hide: false,}" :modules="modules">
        <swiper-slide v-for="(e,index) in 7" :key="index">
          <a href="#">
            <img :src="require(`@/assets/images/prd-item_0${index+1}.jpg`)" alt="e">
          </a>
          <div class="absolute top-48 right-5">
            <a href="#"><img :src="require(`@/assets/images/icon_cart.svg`)" alt="장바구니"></a>
          </div>
          <div class="font-bold text-xs sm:text-sm">{{Prd0[index]}}</div>
          <div class="text-gray-400 text-xs sm:text-sm">{{Prd1[index]}}</div>
          <div class="sm:text-lg md:text-xl lg:text-2xl font-black">{{Prd2[index]}}</div>
          <div class="mt-3 py-2 mb-10">
            <span class="mr-1 border border-red-300 text-red-400 rounded-md text-xs px-1.5 py-1 ">실온</span>
            <span class="border bg-gray-700 text-white rounded-md text-xs px-2 py-1">NEW</span>
          </div>
        </swiper-slide>
        
      </swiper>
    </div>
</template>
<script>
import ContentData from '../../assets/Data.json'


// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';
import 'swiper/css/scrollbar';

// import required modules
import { Scrollbar } from 'swiper';

export default {
  name:"HomeContent_3",
  data() {
    return {
      Prd0 : ContentData.Products.Content_01.Pro1_0,
      Prd1 : ContentData.Products.Content_01.Pro1_1,
      Prd2 : ContentData.Products.Content_01.Pro1_2,
    }
  },
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Scrollbar]
      };
    }
}
</script>
<style>
  
</style>
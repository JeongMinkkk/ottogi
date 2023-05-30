<template>
  <!-- 새로움을 맛보세요 슬라이드 -->
  <div class="max-w-7xl mx-auto h-full mb-20">
    <div class="flex justify-between">
      <h2 class="text-3xl font-extrabold">새로움을 맛보세요</h2>
      <button class="flex">더보기<img :src="require(`@/assets/images/icon_more.svg`)" alt="더보기" class="ml-2"></button>
    </div>
    <swiper class="content_1" :slidesPerView="1" :spaceBetween="10" :breakpoints="{'@0.00': {slidesPerView: 1, spaceBetween: 10,},'@0.75': {slidesPerView: 2,spaceBetween: 20,}, '@1.00': {slidesPerView: 3,spaceBetween: 40,},'@1.50': {slidesPerView: 4,spaceBetween: 50,},}" :modules="modules" :navigation="{prevEl:'.swiper-button-prev',nextEl:'.swiper-button-next'}">
      <swiper-slide v-for="(i,index) in 7" :key="index" class="relative">
        <a href="#"><img :src="require(`@/assets/images/prd-item_0${index+1}.jpg`)" alt="새로움을 맛보세요"></a>
        <div class="absolute top-52 right-1">
          <a href="#"><img :src="require(`@/assets/images/icon_cart.svg`)" alt="장바구니"></a>
        </div>
        <div class="font-bold text-xs sm:text-sm">{{Prd0[index]}}</div>
        <div class="text-gray-400 text-xs sm:text-sm">{{Prd1[index]}}</div>
        <div class="sm:text-lg md:text-xl lg:text-2xl font-black">{{Prd2[index]}}</div>
        <div class="mt-3 py-2">
          <span class="mr-1 border border-red-300 text-red-400 rounded-md text-xs px-1.5 py-1 ">실온</span>
          <span class="border bg-gray-700 text-white rounded-md text-xs px-2 py-1">NEW</span>
        </div>
      </swiper-slide>
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </swiper>
  </div>
</template>
<script>
import ContentData from '../../assets/Data.json'

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
  name:"HomeContent_2",
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
        modules: [Navigation, Pagination]
      };
    }
}
</script>
<style>
.content_1 .swiper-button-prev {
  width: 35px;
  height: 35px;
  /* border: 1px solid #eee; */
  border: 1px solid rgb(226, 226, 226);
  border-radius: 50%;
  background: url(../../assets/images/icon_arrow_left.svg) no-repeat;
  background-size: 50% auto;
  background-position: center;
  top: 170px;

}
.content_1 .swiper-button-next {
  width: 35px;
  height: 35px;
  /* border: 1px solid #eee; */
  border: 1px solid rgb(226, 226, 226);
  border-radius: 50%;
  background: url(../../assets/images/icon_arrow_right.svg) no-repeat;
  background-size: 50% auto;
  background-position: center;
  top: 170px;
}
.content_1 .swiper-button-prev::after,
.content_1 .swiper-button-next::after {
  display: none;
}
</style>
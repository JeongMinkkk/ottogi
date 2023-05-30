<template>
  <div class="w-full">
    <!-- 서브메뉴 -->
    <div class="max-w-7xl mx-auto h-full relative text-center mb-24">
      <ul class="flex flex-wrap justify-around ">
        <li v-for="(e, index) in InnerContent" :key="e" class="hover:font-bold">
          <a href="#" @click.prevent>
            <img :src="require(`@/assets/images/inner_0${index+1}.png`)" :alt="e" class="w-[90px] h-[90px] mt-3">
          </a>
          <a href="#" @click.prevent>
            <p class="text-sm mt-3 tracking-tighter">{{ e }}</p>
          </a>
        </li>
      </ul>
    </div>
    <!-- 새로움을 맛보세요 슬라이드 -->
    <div class="max-w-7xl mx-auto h-full mb-20">
      <div class="flex justify-between">
        <h2 class="text-3xl font-extrabold">새로움을 맛보세요</h2>
        <button class="flex">더보기<img :src="require(`../assets/images/icon_more.svg`)" alt="더보기" class="ml-2"></button>
      </div>
      <swiper  :slidesPerView="1" :spaceBetween="10" :breakpoints="{'@0.00': {slidesPerView: 1, spaceBetween: 10,},'@0.75': {slidesPerView: 2,spaceBetween: 20,}, '@1.00': {slidesPerView: 3,spaceBetween: 40,},'@1.50': {slidesPerView: 4,spaceBetween: 50,},}" :modules="modules" :navigation="{prevEl:'.swiper-button-prev',nextEl:'.swiper-button-next'}" class="mySwiper">
        <swiper-slide v-for="(i,index) in 7" :key="index" class="relative">
          <a href="#"><img :src="require(`@/assets/images/prd-item_0${index+1}.jpg`)" alt="새로움을 맛보세요"></a>
          <div class="absolute top-52 right-1">
            <a href="#"><img :src="require(`../assets/images/icon_cart.svg`)" alt="장바구니"></a>
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
    <!-- 브랜드배너 슬라이드 -->
    <div class="max-w-7xl mx-auto h-full mb-20">
      <div class="basis-full h-32 border rounded-xl">
        <swiper :modules="modules" :navigation="{prevEl:'.swiper-button-prev',nextEl:'.swiper-button-next'}" >
          <swiper-slide v-for="(e,index) in 3" :key="index">
            <a href="#">
              <img :src="require(`@/assets/images/band-bnr_0${index+1}.png`)" alt="e" class="rounded-xl w-full h-32">
            </a>
            <div class="swiper-button-prev"><img :src="require(`@/assets/images/R_arrow_banner.svg`) " alt="슬라이드버튼"></div>
            <div class="swiper-button-next"><img :src="require(`@/assets/images/L_arrow_banner.svg`)" alt="슬라이드버튼"></div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
    <!-- 이런상품 어때요 -->
    <div class="max-w-7xl mx-auto h-full mb-20">
      <h2 class="text-3xl font-bold">이런상품 어때요</h2>
      <swiper :slidesPerView="5" :spaceBetween="10" :freeMode="true" :scrollbar="{hide: false,}" :modules="modules" class="mySwiper">
        <swiper-slide v-for="(e,index) in 7" :key="index">
          <a href="#">
            <img :src="require(`@/assets/images/prd02_0${index+1}.jpg`)" alt="e">
          </a>
          <div class="absolute top-48 right-5">
            <a href="#"><img :src="require(`../assets/images/icon_cart.svg`)" alt="장바구니"></a>
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
    <!--  -->

    <!-- 오뚜기 MD가 엄선 탭 -->
    
    <div class="w-full mx-auto h-full mb-20">
      <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold">오뚜기 MD가 엄선한 갓상품이에요</h2>
        <ul class="flex font-medium text-lg py-6">
          <li  v-for="(e,index) in TabNav" :key="e" @click="TabSelectIndex = index" :class="TabSelectIndex === index && 'font-bold relative after:absolute after:left-0 after:-bottom-1.5 after:border-black after:border-2 after:w-full'" class="mr-5">
            <a href="#" @click.prevent>{{ e }}</a>
          </li>
        </ul>
      </div>
      <div class="">
        <swiper :pagination="false" :modules="modules" class="h-[600px]">
          <swiper-slide v-for="(e,index) in 5" :key="e">
            <img :src="require(`@/assets/images/sub-content0${index+1}.png`)" alt="e" class="relative h-full">
            <div class="absolute max-w-7xl flex top-[35%] left-[16%]">
              <div>
                <h3 class="text-3xl font-black mb-3">나를 위한 오늘의 선택,오뮤</h3>
                <p>롸롸aaaaaaaaaaaa</p>
                <p>롸롸</p>
                <p>롸롸</p>
              </div>
            </div>
            <div class="absolute max-w-7xl flex top-[65%] right-[15%]">
              <div class="border bg-white rounded-lg px-40 py-12 mr-2"> aaaa</div>
              <div class="border bg-white rounded-lg px-40 py-12">bbbbb</div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
    <!-- 지금가장잘팔려요-->
    <div class="max-w-7xl mx-auto h-full mb-20">
      <h2 class="text-3xl font-bold">지금 가장 잘팔려요 </h2>
      <div class="h-60 border border-purple-600"></div>
    </div>
    <!-- 이렇게 먹으면 더 맛있어요 탭-->
    <div class="max-w-7xl mx-auto h-full mb-20">
      <h2 class="text-3xl font-bold">이렇게 먹으면 더 맛있어요</h2>
      <div class="h-96 border border-purple-600"></div>
    </div>
  </div>
</template>
<script>
import ContentData from '../assets/Data.json'

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';

// import required modules
import { Navigation } from 'swiper';
import { Pagination } from 'swiper';
import { Scrollbar } from 'swiper';



export default {
  name:"ContentPage",
  data(){
    return{
      InnerContent : ContentData.Inner,
      // 새로움을 맛보세요
      Prd0 : ContentData.Products.Content_01.Pro1_0,
      Prd1 : ContentData.Products.Content_01.Pro1_1,
      Prd2 : ContentData.Products.Content_01.Pro1_2,
      TabNav : ContentData.Tab.TabNav,
      TabH3: ContentData.Tab.TabH3,
      TabSelectIndex:0,
    }
  },
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation, Pagination, Scrollbar]
      };
    }
    
}
</script>
<style>

</style>
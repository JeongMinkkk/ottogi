<template>
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
        <swiper :pagination="{clickable: true}" :modules="modules" class="h-[600px]">
          <swiper-slide v-for="(e,index) in 5" :key="e">
            <div class="swiper-pagination"></div>
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
  name:"HomeContent_4",
  data() {
    return {
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
        modules: [Navigation, Pagination]
      };
    }
}
</script>
<style>
.swiper-pagination-bullet {
  width: 20px;
  height: 20px;
  text-align: center;
  line-height: 20px;
  font-size: 12px;
  color: #000;
  opacity: 1;
  background: rgba(0, 0, 0, 0.2);
}

.swiper-pagination-bullet-active {
  color: #fff;
  background: #007aff;
}
</style>
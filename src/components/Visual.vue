<template>
  <div class="w-full mb-14 lg:mb-28">
    <!-- swiper 메인슬라이드 -->
    <swiper :pagination="{type: 'fraction',}" :modules="modules" :autoplay="{delay: 3000}" :loop="true" @update=" onSwiperInit">
      <swiper-slide v-for="(e,index) in 7" :key="index" class="h-[300px] sm:h-[350px] md:h-[400px] lg:h-[450px] xl:h-[600px] w-full overflow-hidden">
        <a href=""><img :src="require(`@/assets/images/visual_0${index+1}.jpg`)" :alt="e" class="w-full h-full object-cover"></a>
        <div class="swiper-pagination"></div>
        <!-- <div @click="toggleAutoplay" class="">정지</div> -->
      </swiper-slide>
    </swiper>
  </div>
  
</template>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';
  import 'swiper/css/navigation';

  // import required modules
  import { Pagination, Navigation, Autoplay } from 'swiper';


export default {
  name:"VisualPage",
  components:{
    Swiper,
    SwiperSlide
  },
  setup() {
      return {
        modules: [Pagination, Navigation, Autoplay],
      };
    }
}
</script>
<style>
 .swiper-pagination{
    background: rgba(105, 104, 104, 0.5);
    padding: 8px;
    letter-spacing: 1px;
    width: 70px;
    border-radius: 20px;
    left: 80%;
    margin-bottom: 10px;
    color: white;
    font-size: 12px;
    font-weight: 900;
    
  }

</style>
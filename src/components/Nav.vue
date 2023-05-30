<template>
  <div class="w-full">
    <div class="max-w-7xl mx-auto flex items-center h-[75px] relative">
      <!-- 햄버거메뉴 -->
      <span class="cursor-pointer">
        <div v-for="e in 3" :key="e" class="w-5 lg:w-[22px] h-0.5 bg-black rounded m-1"></div>
      </span>
      <span class="cursor-pointer text-sm lg:text-base ml-2 font-semibold hidden sm:block shrink-0">전체 카테고리</span>
      <!-- 카테고리메뉴 -->
      <!-- <div class="absolute z-10 max-h-[780px]">
        <ul class="border">
          <li v-for="a in CateList" :key="a" class="h-auto overflow-auto bg-white p-4">{{ a }}</li>
        </ul>
      </div> -->
      <!-- 네비-->
      <div class="flex space-x-12 xl:space-x-20 ml-10 sm:mr-10 xl:ml-20 xl:mr-10 cursor-pointer lg:space-x-16 shrink-0">
        <a class="font-bold text-sm lg:text-base" v-for="e in NavList" :key="e">{{ e }}</a>
      </div>
      <!-- 검색 -->
      <div class="text-sm font-semibold mr-9 relative hidden md:block ">
        <input type="text" placeholder="라면은 역시 오뚜기 라면~🍜" class="border rounded-full w-64 h-11 lg:w-[350px] lg:h-[45px] text-center">
        <img :src="require(`@/assets/images/icon_search_21.svg`)" alt="검색" class="absolute top-3.5 right-3 cursor-pointer">
      </div>
      <!-- <img :src="require(`@/assets/images/icon_search_21.svg`)" alt="검색" class="md:hidden"> -->

      <!-- 마이페이지 -->
      <div class="cursor-pointer hidden sm:block sm:ml-10"><a href="#"><img :src="require(`@/assets/images/icon_my.svg`)"  alt="마이페이지"></a></div>
      <!-- 모바일 메뉴 -->
      
    </div>
  </div>

</template>
<script>
import NavData from '../assets/Data.json'

export default {
  name:"NavPage",
  data(){
    return{
      CateList:NavData.Cate,
      NavList:NavData.Nav
    }
  }
}
</script>
<style lang="">
  
</style>
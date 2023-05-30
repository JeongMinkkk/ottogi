<template>
  <!-- 회원가입 팝업 -->
  <div class="w-full bg-[#d3233a]">
    <div class="max-w-7xl mx-auto h-full flex items-center cursor-pointer">
      <div class="basis-full text-center text-white py-3">
        <p>회원가입 시 적립금 1천원 지급!</p>
      </div>
      <button class="pr-2"><img :src="require(`@/assets/images/icon_remove_15.png`)" alt=""></button>
    </div>
  </div>
  <!-- 헤더 -->
  <div class="w-full relative">
    <!-- 로고 -->
    <div class="max-w-7xl mx-auto h-full flex items-center py-8">
      <!-- 모바일검색 -->
      <img :src="require(`@/assets/images/icon_search_21.svg`)" alt="검색" class=" cursor-pointer md:hidden ml-3 sm:ml-10 absolute">
      <div class="mx-auto">
        <a href="#"><img :src="require(`@/assets/images/logo.svg`)" alt="오뚜기로고" title="오뚜기mall"></a>
      </div>
      <!-- 모바일 마이페이지 -->
      <div class="cursor-pointer sm:hidden"><a href="#"><img :src="require(`@/assets/images/icon_my.svg`)" alt="마이페이지"></a></div>
      <!-- 회원가입/로그인/고객센터 -->
      <div class="text-xs text-[#1d1d18] absolute hidden  sm:flex md:gap-x-4 sm:right-2 lg:right-20 xl:right-[330px] ">
        <span class="relative mr-2 md:mr-0 after:left-[50px] after:absolute after:top-2/4 md:after:left-[52px] after:h-3 after:border-l-[1px] after:-translate-y-2/4 "><a href="#">회원가입</a></span>
        <span class="relative mr-2 md:mr-0 after:left-[39px] after:absolute after:top-2/4 md:after:left-[42px]  after:h-3 after:border-l-[1px] after:-translate-y-2/4"><a href="#">로그인</a></span>
        <span class="relative"><a href="#">고객센터</a></span>
      </div>
      

    </div>
  </div>
</template>
<script>
export default {
  name:"HeaderPage",
}
</script>
<style>
  
</style>
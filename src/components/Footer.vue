<template>
  <div class="w-full bg-gray-50">
    <div class="max-w-7xl mx-auto sm:flex sm:justify-between">
      <div class="text-xs sm:text-sm basis-full md:basis-auto">
        <ul class="flex gap-x-8 ml-1 sm:ml-0 items-center mt-16 font-semibold text-gray-800">
          <li v-for="e in FooterMenu" :key="e" class="shrink-0"><a href="#" @click.prevent>{{e}}</a></li>
        </ul>
        <div class="mt-10 tracking-tighter">
          <p class="text-gray-600 mb-2">
            <span class="mr-6 relative after:absolute after:w-[1px] after:h-3 after:bg-[#dfdfdf] after:-right-3 after:top-2/4 after:-translate-y-2/4">대표이사 황성만</span>
            <span class="">14060 경기 안양시 동안구 흥안대로 405(평촌동)</span>
          </p>
          <p class="text-gray-600 mb-2 flex flex-wrap">
            <span class="mr-6 relative after:absolute after:w-[1px] after:h-3 after:bg-[#dfdfdf] after:-right-3 after:top-2/4 after:-translate-y-2/4">사업자 등록번호 138-81-03238 <a href="#" class="underline" @click.prevent>사업자정보확인</a></span>
            <span>통신판매업신고 제 2003-경기안양-169호</span>
          </p>
          <p class="text-gray-600 flex flex-wrap">
            <span class="mr-6 relative after:absolute after:w-[1px] after:h-3 after:bg-[#dfdfdf] after:-right-3 after:top-2/4 after:-translate-y-2/4">건강기능식품 판매업 신고 제 2007-00002호</span>
            <span>개인정보 보호책임 및 청소년보호 책임자 서흥덕</span>
          </p>
          <h3 class="font-bold my-3">KCP 구매안전서비스</h3>
          <div class="flex">
            <p class="text-gray-600 mr-2">
              <span class="leading-6">고객님은 안전거래를 위해 현금 등으로 결제 시 저희 쇼핑몰에서 가입한 <br />구매안전 (에스크로) 서비스를 이용할 수 있습니다.<a href="#" class="underline ml-2" @click.prevent>서비스 가입사실 확인</a></span>
            </p>
            <a href="#" @click.prevent><img :src="require(`@/assets/images/icon_kcp.png`)" alt="인증마크"></a>
          </div> 
        </div>
        
      </div>
      <!-- 오른쪽  -->
      <div class="text-xs sm:text-sm sm:text-right mt-16 basis-full md:basis-auto">
        <p class="md:text-base">고객센터</p>
        <p class="lg:text-3xl font-black my-2">080-433-8888</p>
        <p class="tracking-tighter">월~금 09:00~17:00</p>
        <p class="tracking-tighter">(점심시간 12:30~13:00)</p>
        <div class="flex mt-5 gap-x-8">
          <div v-for="e in 4" :key="e" @click.prevent><a href="#"><img :src="require(`@/assets/images/icon_sns_0${e}.png`)" alt=""></a></div>
        </div>
      </div>
    </div>
    <div class="max-w-7xl mx-auto flex items-center py-10">
        <p class="text-gray-700 mr-5">Copyright ⓒ ottogimall.co.kr</p>
        <a href="#" class="mr-5" @click.prevent><img :src="require(`@/assets/images/icon_company.png`)" alt="로고"></a>
        <a href="#" @click.prevent><img :src="require(`@/assets/images/icon_okitchen.png`)" alt="로고"></a>
    </div> 
  </div>
</template>
<script>
export default {
  name:"FooterPage",
  data(){
    return{
      FooterMenu:["오뚜기몰 존재이유","고객센터","이용약관","개인정보처리방침","대량주문문의"]
    }
  }
}
</script>
<style>
  
</style>

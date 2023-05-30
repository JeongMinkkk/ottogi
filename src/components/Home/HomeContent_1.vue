<template>
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
</template>
<script>
import ContentData from '../../assets/Data.json'
export default {
  name:"HomeContent_1",
  data() {
    return {
      InnerContent : ContentData.Inner,
    }
  },
}
</script>
<style>

</style>
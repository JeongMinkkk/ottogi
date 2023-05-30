<template>
  <Header />
  <Nav />
  <HomeVisual />
  <div class="w-full">
    <HomeContent_1 />
    <HomeContent_2 />
    <HomeBanner />
    <HomeContent_3 />
    <!-- <HomeContent_4 />
    <HomeContent_5 />
    <HomeContent_6 /> -->
  </div>
  <Footer />
</template>

<script>
import Header from './components/Header.vue'
import Nav from './components/Nav.vue'
import HomeVisual from './components/Home/HomeVisual.vue'
import HomeContent_1 from './components/Home/HomeContent_1.vue'
import HomeContent_2 from './components/Home/HomeContent_2.vue'
import HomeBanner from './components/Home/HomeBanner.vue'
import HomeContent_3 from './components/Home/HomeContent_3.vue'
// import HomeContent_4 from './components/Home/HomeContent_4.vue'
// import HomeContent_5 from './components/Home/HomeContent_5.vue'
// import HomeContent_6 from './components/Home/HomeContent_6.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Nav,
    HomeVisual,
    HomeContent_1,
    HomeContent_2,
    HomeBanner,
    HomeContent_3,
    // HomeContent_4,
    // HomeContent_5,
    // HomeContent_6,
    Footer
  }
}
</script>

<style>

</style>

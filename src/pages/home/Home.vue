<template>
  <div>
    <home-head></home-head>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHead from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHead,
    HomeSwiper,
    HomeIcons
  }
}
</script>

<style>
.test {
  color: aqua;
}
</style>

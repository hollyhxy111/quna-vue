<template>
  <div>
    <home-head></home-head>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHead from './components/Header'
import HomeSwiper from './components/Swiper'
export default {
  name: 'Home',
  components: {
    HomeHead,
    HomeSwiper
  }
}
</script>

<style>
.test {
  color: aqua;
}
</style>

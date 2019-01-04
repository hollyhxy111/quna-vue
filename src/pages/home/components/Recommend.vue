<template>
  <div>
    <div class="guess-u-like">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '上海迪士尼乐园拥有七大主题园区：米奇大街、奇想花园、梦幻世界、探险岛、宝藏湾、明日世界和迪士尼•皮克斯玩具总动员主题园区'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '上海迪士尼乐园拥有七大主题园区：米奇大街、奇想花园、梦幻世界、探险岛、宝藏湾、明日世界和迪士尼•皮克斯玩具总动员主题园区'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '上海迪士尼乐园拥有七大主题园区：米奇大街、奇想花园、梦幻世界、探险岛、宝藏湾、明日世界和迪士尼•皮克斯玩具总动员主题园区'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.guess-u-like
  margin-top: 1rem
  line-height: 2rem
  background: #eee
  text-indent: .4rem
.item
  overflow: hidden
  display: flex
  height: 6rem
  .item-img
    width: 5.4rem
    height: 5.4rem
    padding: .3rem
  .item-info
    flex: 1
    padding: .2rem
    min-width: 0
    .item-title
      line-height: 1.5rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: 1.5rem
      font-size: .28rem
      color: #ccc
      ellipsis()
    .item-btn
      // line-height: 1rem
      margin-top: .7rem
      background: #ff9300
      padding:  .1rem .4rem
      border-radius: .5rem
      color: #fff
</style>

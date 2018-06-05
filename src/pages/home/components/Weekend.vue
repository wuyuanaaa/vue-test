<template>
  <div>
    <div class="title">活动列表</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl'>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://m.ykclass.com/zt/jianzao2/1/images/banner.jpg',
        title: '中级会计实务',
        desc: '中级会计实务名师体验课中级会计实务名师体验课'
      }, {
        id: '0002',
        imgUrl: 'http://m.ykclass.com/zt/tdxl/1/images/banner-425m.jpg',
        title: '同等学力',
        desc: '中级会计实务名师体验课中级会计实务名师体验课'
      }, {
        id: '0003',
        imgUrl: 'http://m.ykclass.com/zt/cjkjzc/1/images/m.jpg',
        title: '初级会计职称',
        desc: '中级会计实务名师体验课中级会计实务名师体验课'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height: 0
    padding-bottom 33.9%
    .item-img
      width: 100%
  .item-info
    padding .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()

</style>

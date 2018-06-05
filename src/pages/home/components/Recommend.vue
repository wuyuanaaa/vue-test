<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src='item.imgUrl'>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/4/11/df9f0a1a84a64b21af3cfa316b1878d9.jpg',
        title: '1中级会计实务中级会计实务中级会计实务中级会计实务',
        desc: '中级会计实务名师体验课中级会计实务名师体验课'
      }, {
        id: '0002',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/4/11/df9f0a1a84a64b21af3cfa316b1878d9.jpg',
        title: '2中级会计实务中级会计实务中级会计实务中级会计实务',
        desc: '中级会计实务名师体验课中级会计实务名师体验课'
      }, {
        id: '0003',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/4/11/df9f0a1a84a64b21af3cfa316b1878d9.jpg',
        title: '3中级会计实务中级会计实务中级会计实务中级会计实务',
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
  .item
    display flex
    height: 1.9rem
    overflow hidden
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background: #ff9300
        padding 0 .2rem
        border-radius .06rem
        color: #fff

</style>

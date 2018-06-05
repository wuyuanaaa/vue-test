<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src='item.imgUrl'>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/2/2/37f87419f6384349b58f4fb664eee4b1.png',
        desc: '中级会计'
      }, {
        id: '0002',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/2/2/ebd4a14bdff94bc8b1e87a73e69d25ed.png',
        desc: '法律职业资格'
      }, {
        id: '0003',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/0/19/4e92eb32fdd24c9792f47f8f69574e4a.png',
        desc: '教师资格'
      }, {
        id: '0004',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/2/2/40fdc912dbae4122b6c40b767d96cf5e.png',
        desc: '统计师'
      }, {
        id: '0005',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/2/2/73ae9b5cb71d4c4a8b420492d02baab4.png',
        desc: '高级会计'
      }, {
        id: '0006',
        imgUrl: 'https://img1.ykclass.com/img/paths/2017/11/24/4d8a349c57d7431ba49f54ff22d86b08.png',
        desc: '公务员'
      }, {
        id: '0007',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/2/2/1747446b63f446ddbf6b8816cadfe5da.png',
        desc: '社会工作者'
      }, {
        id: '0008',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/4/3/3ebbe105250442588fca2d6ca4ddd81b.png',
        desc: '银行专业资格'
      }, {
        id: '0009',
        imgUrl: 'https://img1.ykclass.com/img/paths/2018/3/27/1865bca5fb9141db9683fd79344d838c.png',
        desc: '事业单位'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    margin-top .2rem
    .icon
      position relative
      overflow hidden
      float: left
      width: 25%
      height: 0
      padding-bottom 25%
      .icon-img
        position absolute
        top: 0
        left: 0
        right: 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        .icon-img-content
          display block
          margin 0 auto
          height: 100%
      .icon-desc
        position absolute
        left: 0
        right: 0
        bottom: 0
        height .44rem
        line-height .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()

</style>

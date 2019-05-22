<template>
  <div class="container">
    <div class="recommend-title">本周热门榜单</div>
    <div class="border-right">全部榜单</div>
    <ul class="container-ul">
      <li class="item" v-for="item of swiperList" :key="item.id">
        <div class="items-img-wrapper">
          <img class="img-item" :src="item.imgUrl" :alt="item.name" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.name}}</p>
          <p class="item-desc">{{item.price}}</p>
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
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/f1/f19afcb3a640ebd1a3.water.jpg_250x250_41ea1dea.jpg',
        name: '大昭寺',
        price: '35'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1901/8e/8e36f8d630abdaf3a3.img.jpg_250x250_87ea15ae.jpg',
        name: '清水河老牛湾',
        price: '35'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/f1/f19afcb3a640ebd1a3.water.jpg_250x250_41ea1dea.jpg',
        name: '哈素海天鹅温泉堡',
        price: '86'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1504/69/699ea4ce566de816.water.jpg_250x250_380ba3fb.jpg',
        name: '神泉生态旅游景区',
        price: '35'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1705/a2/a23dfca36b89d846a3.water.jpg_250x250_144a490f.jpg',
        name: '蒙亮蒙古风情园',
        price: '35'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1901/29/291562d5579a185aa3.img.jpg_250x250_7c54b369.jpg',
        name: '乐汤汇温泉生活馆',
        price: '35'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container
    margin-top: .3rem
    .recommend-title
      width: 0.5rem
      height: 1.0rem
      display: inline
      margin-left: .4rem
    .border-right
      margin-right: .4rem
      float: right
    .container-ul
      white-space: nowrap
      overflow-x: scroll
      padding 0.2rem
      .item
        width: 2rem
        height: 3rem
        position: relative
        display: inline-block
        padding: .06rem
        .items-img-wrapper
          width: 2rem
          height: 2rem
          overflow: hidden
          .img-item
            width:100%
        .item-info
          display: block
          padding-top: .1rem
          width: 2rem
          height: 1rem
          text-align: center
          .item-title
            hight: 0.2rem
            font-size: 0.1rem
            line-height: 0.2rem
          .item-desc
            hight: 0.4rem
            font-size: 0.3rem
            line-height: 0.4rem
          .item-button
            hight: 0.2rem
            font-size: 0.15rem
            line-height: 0.2rem
</style>

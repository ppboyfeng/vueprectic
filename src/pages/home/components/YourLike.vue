<template>
  <div>
    <ul class="total-list">
      <div class="title"><span class="iconfont like-icon">&#xe632;</span>猜你喜欢</div>
      <li class="item" v-for="item of List" :key="item.id">
        <div class="container">
          <div class="img-container">
            <img class="img-set" :src="item.imgUrl" :alt="item.name">
          </div>
            <div class="right-wrapper">
            <div class="name">{{item.name}}</div>
            <div class="zan" mp-role="star" :data-score="item.stars">{{item.discussion}}条评论</div>
            <div class="right-bottom">
              <span class="price">{{item.price}}</span>
              <span class="address">{{item.address}}</span>
            </div>
            <span></span>
          </div>
        </div>
      </li>
    </ul>
    <a class="border" href="">查看所有商品</a>
  </div>
</template>

<script>
export default {
  name: 'HomeYourLike',
  data () {
    return {
      List: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg',
        name: '北京世界园艺博览会',
        stars: '4.7',
        discussion: '650',
        price: '108',
        address: '延庆县'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg',
        name: '北京世界园艺博览会',
        stars: '',
        discussion: '',
        price: '35',
        address: '延庆县'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg',
        name: '北京世界园艺博览会',
        stars: '',
        discussion: '',
        price: '35',
        address: '延庆县'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg',
        name: '北京世界园艺博览会',
        stars: '',
        discussion: '',
        price: '35',
        address: '延庆县'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg',
        name: '北京世界园艺博览会',
        stars: '',
        discussion: '',
        price: '35',
        address: '延庆县'
      } ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .total-list
    margin-left: 0.2rem
  .title
    font-size:0.35rem
    line-height: 1.0rem
    hight: 1.0rem
    .like-icon
      ext-align: left
      font-size: .4rem
      display: inline-block
      margin-right: 0.1rem
  .item
    height: 2.4rem
    border-bottom: 0.03rem solid #e0e0e0
    display: block
    .container
      height: 2.4rem
      display: block
      padding: 0.2rem 0rem
      .img-container
        height: 2.0rem
        width: 2.0rem
        background: black
        float: left
        overflow: hidden
        .img-set
          width:100%
      .right-wrapper
        padding-left: 0.22rem
        overflow: hidden
        display: block
        .name
          margin-top: .26rem
          height: .44rem
          color: #212121
          font-size: .32rem
          line-height: .44rem
          ellipsis()
        .zan
          color: #616161
          font-size: .24rem
          line-height: .34rem
        .right-bottom
          margin: .22rem 0rem
          position: relative
          color: #616161
          font-size: .24rem
          line-height: .4rem
          .price
            color: #ff8300
            font-size: .4rem
            line-height: 0.4rem
            display inline-block
          .address
            position: absolute
            right: .24rem
            bottom: 0
            color: #616161
            font-size: .24rem
            line-height: .4rem
  .border
    height: 1.2rem
    display: block
</style>

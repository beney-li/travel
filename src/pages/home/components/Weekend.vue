<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
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
export default{
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海海洋公园',
        desc: '浪漫的上海首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海海洋公园',
        desc: '浪漫的上海首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海海洋公园',
        desc: '浪漫的上海首站，浪漫的海洋主题乐园'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title{
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  }
    .item-img-wrapper{
      height: 0
      overflow: hidden
      padding-bottom: 37.9%
    }
  .item-img{
    width: 100%
  }
    .item-info{
      padding: .1rem
    }
  .item-title{
    line-height: .54rem
    font-size: .32rem
    ellipsis()
  }
  .item-desc{
    line-height: .4rem
    color: #ccc
    ellipsis()
  }
</style>

<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img"
             :src="item.imgUrl"/>
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
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/a3/a37ced8252b273c9.img.jpg_150x150_8eea713b.jpg',
          title: '夫子庙秦淮河游船',
          desc: '夜泊秦淮近酒家，桨声灯影里的秦淮河'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201305/22/273c38aa938ad97dc8d65eac.jpg_150x150_964040ab.jpg',
          title: '夫子庙秦淮河游船',
          desc: '夜泊秦淮近酒家，桨声灯影里的秦淮河'
        }, {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1512/95/9579bcb3e5a206cc90.water.jpg_150x150_2b0229bc.jpg',
          title: '夫子庙秦淮河游船',
          desc: '夜泊秦淮近酒家，桨声灯影里的秦淮河'
        }]
      }
    }

  }
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem

  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipse()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipse()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
        color: #fff
</style>

<template>
  <div class="dashboard-container">
    <div class="dashboard-text">
      <div class="container"></div>
    </div>
  </div>
</template>

<script>
import service from '@/utils/request'
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  
  data(){
    return {
      goods:[
        {
          goodsType:"饮料",
          goodsArr:[
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
          ],
        },
        {
          goodsType:"饮料",
          goodsArr:[
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
          ],
        },
        {
          goodsType:"饮料",
          goodsArr:[
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
            {
              Name:'可口可乐500ml',
              imgUrl:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.defanli.com%2Fi3%2F2208182652164%2FO1CN01wtAPta1Rr9lTVqfbX_%21%212208182652164.jpg_q90.jpg&refer=http%3A%2F%2Fimg.defanli.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651654933&t=67682a4b831f872f1eb8853df433a4a6',
              price:'3'
            },
          ],
        },
      ]
    }
  },
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
.container{
    width: 100px;
    height: 100px;
   background: rgb(168, 157, 157); 
  }
</style>

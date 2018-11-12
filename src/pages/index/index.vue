<template>
  <div class="container" @click="clickHandle('test click', $event)">
    <view class="tabHeader">
      <span v-for='(tab ,index) in tabs' :key='index'
        :class=" currentPage==tab.id ? 'on li': 'li' "
        @click="changeTab(tab.id)">{{tab.name}}</span>  
    </view>
    <div class="conList">
      <contentList :text='follow'/>
      <contentList :text='hot'/>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'
import contentList from '@/components/contentList'

export default {
  data () {
    return {
      userInfo: {},
      tabs:[{id: 'follow', name: '关注'}, {id: 'hot', name: '热门'}],
      currentPage: 'follow'
    }
  },

  components: {
    card,
    contentList
  },

  methods: {
    myMusic () {
      const url = '../music/main'
      wx.navigateTo({ url })
    },
    getUserInfo () {
      // 调用登录接口
      wx.login({
        success: () => {
          wx.getUserInfo({
            success: (res) => {
              this.userInfo = res.userInfo
            }
          })
        }
      })
    },
    clickHandle (msg, ev) {   // 打印点击处的信息    
      // console.log('clickHandle:', msg, ev)
    },
    changeTab (msg) {
      this.currentPage = msg
    }
  },

  created () {
    // 调用应用实例的方法获取全局数据
    this.getUserInfo()
  }
}
</script>

<style scoped>
.tabHeader {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width:100%;
  background-color:#eee;
  height:95rpx;
}
.on{
  color: #FF4500;  
  border-bottom: 5rpx solid #FF4500;
}
.li{
  padding:0 20rpx;
  line-height:90rpx;
}

</style>

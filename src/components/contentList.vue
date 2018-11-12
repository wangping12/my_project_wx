<template>
  <div class="conList">
    <view class="title">
      <img src="../../static/img/head2.jpg" class="imgHead"/>
      <view class="headCenter">
        <view class="headName">小瓶子</view>
        <span class="headFrom">2018-11-12 来自weibo.com</span>
      </view>
      <view class="isFollow">+ 关注</view>
    </view>
    <view class="content">
      女孩 不想看你受一样的伤害 所以学会溺爱 一而再 再而再 三而再 的错怪 到底要什么姿态 才不会显得我太直白 大门不出 二门不迈 想带你一起走出门外 去植物园里晒晒 去鼓浪屿上看海 满足你眼神里的期待 在中山路上买买 马蹄酥全装起来 为了你眼神里的崇拜 女孩 我的故事因为你而展开 为你学会忍耐 为你 坏习惯我都改 女孩 不想看你受一样的伤害 所以学会溺爱 错怪 你真正要的爱 去植物园里晒晒 去鼓浪屿上看海 满足你眼神里的期待
    </view>
  </div>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style>
.conList {
  width: 100%;
  display: flex;
  flex-direction: column;
  padding-top: 10rpx;
}
.title{
  display: flex;
  flex-direction: row;
}
.imgHead{
  border-radius: 50%;
  width: 120rpx;
  height: 100rpx;
}
.headCenter{
  width: 80%;
  display: flex;
  flex-direction: column;
  padding-left:15rpx;
}
.headName{
  width: 100%;
}
.headFrom{
  font-size: 30rpx;
}
.isFollow{
  width: 155rpx;
  height: 60rpx;
  border: 5rpx solid #FFB90F;
  border-radius: 10%;
}
.content{
  padding: 10rpx;
  text-indent: 2em;
}
</style>

<template>
  <view class="box">
    <view
      data-url="{{item.url}}"
      key="{{item.index}}"
      wx:for="{{data}}"
      wx:for-item="item"
      wx:for-index="index"
      bindtap="onClick"
    >
      <view class="bd">
        <img src="https://img.alicdn.com/tfs/TB1bLoWoYH1gK0jSZFwXXc7aXXa-684-684.png" class="layer" />
        <img src="{{item.coverImage}}" class="bg" />
        <view class="wrap">
          <img src="https://img.alicdn.com/tfs/TB1mtZRoVT7gK0jSZFpXXaTkpXa-28-36.png" class="riverdinwei" />
          <text class="distance">距离500m</text>
        </view>
      </view>
      <view class="main">
        <text class="title">{{item.title}}</text>
      </view>
      <view class="ft">
        <view class="block">
          <img src="https://img.alicdn.com/tfs/TB1OvsYoW61gK0jSZFlXXXDKFXa-60-60.png" class="xianjin" />
          <text class="fashion-home">{{item.user.userName}}</text>
        </view>
        <view wx:if="{{isReadCountShow(item.readCount)}}" class="group">
          <img src="https://img.alicdn.com/tfs/TB1arwYo7T2gK0jSZFkXXcIQFXa-46-44.png" class="favorite" />
          <text class="num">{{item.readCount}}</text>
        </view>
      </view>
    </view>
  </view>
</template>

<script lang="ts" src="./index.ts">
</script>
    
<style lang="scss" scoped>
  @import url('./index.scss');
</style>
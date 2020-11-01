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
                <text class="title">{{ item.title }}</text>
            </view>
            <view class="ft">
                <view class="block">
                    <img src="https://img.alicdn.com/tfs/TB1OvsYoW61gK0jSZFlXXXDKFXa-60-60.png" class="xianjin" />
                    <text class="fashion-home">{{ item.user.userName }}</text>
                </view>
                <view wx:if="{{isReadCountShow(item.readCount)}}" class="group">
                    <img src="https://img.alicdn.com/tfs/TB1arwYo7T2gK0jSZFkXXcIQFXa-46-44.png" class="favorite" />
                    <text class="num">{{ item.readCount }}</text>
                </view>
            </view>
        </view>
    </view>
</template>

<script>
export default {
    data() {
        return {};
    },
    onLoad() {
        console.log('页面加载完成');
    },
    methods: {}
};
</script>

<style lang="scss" scoped>
.box {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: flex-start;
    height: 534rpx;
}
.bd {
    display: flex;
    position: relative;
    align-items: flex-start;
    flex-direction: row;
    opacity: 1;
    width: 342rpx;
    height: 342rpx;
}
.layer {
    position: absolute;
    top: 0rpx;
    left: 0rpx;
    width: 342rpx;
    height: 342rpx;
    overflow: hidden;
}
.bg {
    position: absolute;
    top: 0rpx;
    left: 0rpx;
    opacity: 1;
    width: 342rpx;
    height: 342rpx;
}
.wrap {
    box-sizing: border-box;
    display: flex;
    position: relative;
    align-items: center;
    flex-direction: row;
    margin-top: 18rpx;
    margin-left: 18rpx;
    border-radius: 15rpx;
    background-color: rgba(0, 0, 0, 0.4);
    padding-right: 9rpx;
    padding-left: 10rpx;
    height: 30rpx;
}
.riverdinwei {
    opacity: 1;
    width: 14rpx;
    height: 18rpx;
}
.distance {
    margin-left: 4rpx;
    height: 22rpx;
    font-weight: 400;
    font-size: 18rpx;
    color: #ffffff;
    line-height: 22rpx;
    white-space: nowrap;
}
.main {
    display: flex;
    align-items: flex-start;
    flex-direction: row;
    justify-content: center;
    background-color: #ffffff;
    width: 342rpx;
    height: 114rpx;
}
.title {
    margin-top: 22rpx;
    width: 300rpx;
    height: 88rpx;
    font-weight: 400;
    font-size: 30rpx;
    color: #333333;
    line-height: 44rpx;
    overflow: hidden;
    text-overflow: ellipsis;
}
.ft {
    box-sizing: border-box;
    display: flex;
    align-items: center;
    flex-direction: row;
    justify-content: space-between;
    border-bottom-left-radius: 12rpx;
    border-bottom-right-radius: 12rpx;
    background-color: #ffffff;
    padding-right: 17rpx;
    padding-left: 18rpx;
    width: 342rpx;
    height: 78rpx;
    overflow: hidden;
}
.block {
    display: flex;
    align-items: center;
    flex-direction: row;
    height: 30rpx;
}
.xianjin {
    width: 30rpx;
    height: 30rpx;
}
.fashion-home {
    margin-left: 6rpx;
    height: 28rpx;
    font-weight: 300;
    font-size: 24rpx;
    color: #666666;
    line-height: 28rpx;
    white-space: nowrap;
}
.group {
    display: flex;
    align-items: center;
    flex-direction: row;
    height: 30rpx;
}
.favorite {
    width: 22rpx;
    height: 22rpx;
}
.num {
    margin-left: 5rpx;
    height: 26rpx;
    font-weight: 400;
    font-size: 22rpx;
    color: #999999;
    line-height: 26rpx;
    white-space: nowrap;
}
</style>

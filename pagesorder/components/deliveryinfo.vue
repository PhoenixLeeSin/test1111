/**
 * 订单结算页下配送信息组件 
 */
<template>
  <view class="container">
      <view class="header">
        <view v-if="item.canDelivery === 1" class="header-item" :class="{'tabactive':item.seltab===1}" @click="changeTab(1)">配送到家</view>
        <view class="header-item" :class="{'tabactive':item.seltab===2}" @click="changeTab(2)">到店自取</view>
      </view>
      <view class="content">
        <!-- 骑手配送 -->
        <view v-if="item.canDelivery === 1 && item.seltab===1" class="delivery">
          <view class="leftflex border" @click="gotoMyAddress">
            <view class="common-flex">
              <view class="common-bigtitle common-bluetitle common-padding ">{{ item.selAddress }}</view>
            </view>
            <view>
              <!-- 注释掉此代码正常 -->
              <!-- <u-icon name="arrow-right" size="36rpx" color="#757575"></u-icon> -->
            </view>
          </view>
        </view>
      </view>   
  </view>
</template>

<script>
  export default {
    props: {
      item: {
        type: Object,
        default: function () {
          return {}
        }
      },
    },
    data () {
      return {
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>

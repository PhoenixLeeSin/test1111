<template>
  <view>
    <view>我是父组件</view>
    <deliveryinfo :item="item"></deliveryinfo>
  </view>
</template>

<script>
  import deliveryinfo from '../components/deliveryinfo.vue'
  export default {
    components: {
      deliveryinfo
    },
    data() {
      return {
        item: {
          canDelivery: 1,
          selAddress: "选择收货地址",
          selfContactResponse: {
            contactPerson: "李",
            contactPhone: "15269241990"
          },
          seltab: 1,
          shopAddress: "青岛市市北区伊春路104、106号"
        }
      }
    },
    onLoad() {
    }
  }
</script>

<style>
</style>

<template>
  <view class="index">
    <button openType="getUserInfo" onGetUserInfo="getInfo">授权登录</button>
  </view>
</template>

<script>
import Taro from '@tarojs/taro'
import './index.scss'

export default {
  data () {
    return {
      msg: 'Hello world!'
    }
  },
  methods: {
    // 触发不了
    getInfo(res) {
      console.log('res', res)
    }
  },
  mounted() {
    // 授权后正常
    Taro.getUserInfo({
      success: function(res) {
        console.log('1111', res)
      }
    })
  }
}
</script>

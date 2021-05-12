<template>
  <view class="page">
    <view class="demo-header">
      <text class="demo-title">基础样式</text>
    </view>
    <view class="demo-container">
      <view class="demo-item">
        <view class="item-title">
          <text class="item-title-text">盒模型</text>
        </view>
        <view class="item-container">
          <view class="box-container">
            <view class="box-item">
              <view class="box-content">
                <text>Box Content</text>
              </view>
            </view>
          </view>
        </view>
      </view>
      <view class="demo-item">
      <view class="item-title">
        <text class="item-title-text">Font Style</text>
        </view>
        <view class="item-container">
          <view class="box-container">
            <text :class="['tab', isBold? 'active': '']">Box Content</text>
          </view>
          <view class="operation-container">
            <button class="btn" @tap="toggleFontWeight">
              toggle style
            </button>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>
<style lang="less" scoped>
.page {
  background-color: #eeeeee;
  margin-bottom: 0.5rem;
}
.demo-header {
  padding: 0.2rem 0;
  background-color: #fa9153;
}
.demo-title {
  font-size: 0.36rem;
  width: 100%;
  text-align: center;
  color: white;
}
.demo-container {
  margin-top: 0.2rem;
}
.demo-item {
  background-color: #ffffff;
  width: 100%;
  margin-bottom: 0.2rem;
  padding: 0.2rem 0;
}
.item-title {
  text-align: center;
}
.item-title-text {
  text-align: center;
  font-size: 0.28rem;
}
.item-container {
  margin-top: 0.2rem;
}
.box {
  width: 1rem;
  height: 1rem;
  margin: 0.1rem;
  background-color: #fa9153;
}
.box-flex-row {
  display: flex;
  flex-direction: row;
}
.operation-container {
  display: flex;
  justify-content: space-between;
}
.btn {
  flex: 1;
  margin: 0 0.2rem;
  height: 0.8rem;
  text-align: center;
  color: white;
  background: #fa9153;
  border-radius: 10px;
}
.box-item {
  width: 4rem;
  height: 4rem;
  background-color: #eeeeee;
  padding: 0.5rem;
  border: 0.2rem solid blue;
}
.box-content {
  background-color: red;
  width: 100%;
  height: 100%;
}

// custom
.font-bold{
  font-weight: bold;
}
.font-normal{
  font-weight: normal;
}
.tab{
  text-align: center;
  font-size: 0.32rem;
  height: 1.2rem;
  line-height: 1.2rem;
  font-weight: normal;
  color: #999;
}
.active{
  // font-size: 0.36rem;
  font-weight: bold;
  color:#fa9153;
}
</style>

<script>
export default {
  data() {
    return {
      isBold: false
    };
  },
  methods: {
    toggleFontWeight(){
      this.isBold = !this.isBold
    }
  }
};
</script>
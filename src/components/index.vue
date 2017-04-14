<template>
  <div class="index-container">
    <div class="index-header">
      <div class="header-box">
        <div class="me">我的</div>
        <div class="recommend">推荐</div>
        <div class="discovery">发现</div>
      </div>
    </div>
    <div class="menu"></div>
    <div class="search"></div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  .index-container {
    .index-header {
      height: 42px;
      background: #f83;
      .header-box {
        display: flex;
        font-size: 16px;
        color: #ffd5b7;
        &>div {
          flex: 1;
          line-height: 42px;
        }
        .me {
          text-align: right;
        }
        .recommend {
          text-align: center;
        }
        .discovery {
          text-align: left;
        }
      }
    }
  }
</style>

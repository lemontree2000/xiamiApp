<template>
  <div class="recommend">
    <div class="recommend-header">
      <div class="scene-bar">
        <span class="scene-logo">场景音乐</span>
        <span class="go-icon"></span>
      </div>
      <div class="quick-list">
        <ul class="quick-box">
          <li class="quick-item">
            <div class="image-box">
              <img src="../assets/image/14671842274837.png" alt="">
            </div>
            <span class="item-title">跑步</span>
          </li>
        </ul>      
      </div>
    </div>
    <div class="recommend-other">
      <ul>
        <li class="other-item">
          <span class="other-icon"></span>
          <div class="other-content">
            <span class="other-title">社区</span>
            <span class="other-sub">VIP专属福利</span>
            <span class="go-icon"></span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  
</script>

<style lang="less" scoped>
  .recommend {
    background: #f8f8f8;
    .recommend-header {
      background: #fff;
      .scene-bar {
        height: 55px;
        line-height: 55px;
        border-bottom: 1px solid #e6e6e6;
        padding: 0 19px;
        font-size: #323232;
      }
      .quick-list {
        .quick-box {
          font-size: 0;
          .quick-item {
            width: 25%;
            display: inline-block;
          }  
        }  
      }
    }
  }
</style>

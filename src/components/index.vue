<template>
  <div class="index-container">
    <div class="index-header">
      <div class="header-box">
        <div class="me" @click="showComp('v-my',1)" :class="{'active': currState==1}">我的</div>
        <div class="recommend" @click="showComp('v-recommend',2)" :class="{'active': currState==2}">推荐</div>
        <div class="discovery" @click="showComp('v-discovery',3)" :class="{'active': currState==3}">发现</div>
      </div>
      <div class="menu"></div>
      <div class="search"></div>
    </div>
    <component :is="currComp"></component>
  </div>
</template>

<script>
import recommend from '../components/recommend'
import discovery from '../components/discovery'
import my from '../components/my'

export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      currComp: 'v-recommend',
      currState: 2
    }
  },
  components: {
    'v-recommend': recommend,
    'v-discovery': discovery,
    'v-my': my
  },
  methods: {
    showComp (comId, state) {
      console.log(comId, state)
      this.currComp = comId
      this.currState = state
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  .index-container {
    .index-header {
      position: relative;      
      height: 42px;
      background: #f83;
      .header-box {
        display: flex;
        font-size: 16px;
        color: #ffd5b7;
        &>div {
          flex: 1;
          line-height: 42px;
          &.active {
            color: #fff;
          }
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
    .menu {
      position: absolute;
      top: 50%;
      margin-top: -1px;;
      left: 17px;
      width: 22px;
      height: 2px;
      background: #fff;
      border-radius: 1px;
      &::before {
        content: '';
        position: absolute;
        top: 5px;        
        width: 22px;
        height: 2px;
        background: #fff;
        border-radius: 1px;
      }
      &::after {
        content: '';        
        position: absolute;        
        bottom: 5px;
        width: 22px;
        height: 2px;
        background: #fff;
        border-radius: 1px;
      }
    }
    .search {
      position: absolute;
      right: 16px;
      top: 50%;
      margin-top: -10px;
      width: 20px;
      height: 20px;
      background: url('../assets/image/index@search.png') no-repeat 0 0;
      background-size: 20px 20px;
    }
  }
</style>

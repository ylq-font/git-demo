<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if = '!isActive'><slot  name="item-icon"></slot></div>
    <div v-else><slot  name = 'item-icon-active'></slot></div>
    <div :style="activeStyle"><slot name="item-text">我的</slot></div>
  </div>
</template>

<script>
export default {
  name:'TabBarItem',
  props:{
    path:String,
    activeColor:{
      type:String,
      default:'red'
    }
  },
  data(){
    return{
      // isActive:true
    }
  },
  computed: {
    isActive(){ 
      // indexOf:判断是否相等
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle(){
      // 判断是否处于活跃
      // 若处于活跃则颜色改为blue
      // 不处于活跃则为默认红色 
      return this.isActive ? {color:this.activeColor} : {}
    }
  },
  methods: {
    itemClick(){
      this.$router.replace(this.path)
    }
  },
}
</script>

<style>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size:14px;
  }
  .iconfont{
    font-size: 25px;
    margin-top:1px;
    vertical-align:middle;
  }
  .home{
    margin-top: -3px;
  }
</style>
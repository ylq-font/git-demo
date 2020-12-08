<template>
  <tab-bar>
    <TabBarlItem path='/home' >
      <div class="iconfont icon-icon_home" slot='item-icon'></div>
      <div class="iconfont icon-home" slot='item-icon-active'></div>
      <div slot='item-text'>首页</div>
    </TabBarlItem>
    <TabBarlItem path='/category' >
      <div class="iconfont icon-fenlei1" slot='item-icon'></div>
      <div class="iconfont icon-fenlei" slot='item-icon-active'></div>
      <div slot='item-text'>分类</div>
    </TabBarlItem>
    <TabBarlItem path='/cart' >
      <div class="iconfont icon-gouwuchekong" slot='item-icon'></div>
      <div class="iconfont icon-gouwucheman" slot='item-icon-active'></div>
      <div slot='item-text'>购物车</div>
    </TabBarlItem>
    <TabBarlItem path='/profile' >
      <div class="iconfont icon-mine" slot='item-icon'></div>
      <div class="iconfont icon-mine-red" slot='item-icon-active'></div>
      <div slot='item-text'>我的</div>
    </TabBarlItem>
  </tab-bar>
</template>

<script>
import TabBar from './tabbar/TabBar'
import TabBarlItem from './tabbar/TabBarItem'
export default {
  name:'MainTabBar',
  components:{
    TabBar,
    TabBarlItem
  }
}
</script>

<style>

</style>
<template>
  <div class="layout">
<!--    左侧导航-->
    <div class="menu">
      <Menu :isCollapse="isCollapse"></Menu>
    </div>
<!--    右侧内容-->
    <div class="content" :class="{small:isCollapse}">
      <Content @changeShow="changeShow" :isCollapse="isCollapse"></Content>
    </div>
  </div>
</template>

<script>
import Menu from './menu/Index.vue'
import Content from './content/Index.vue'
export default {
  components:{
    Menu,
    Content
  },
  data(){
    return {
      isCollapse: false
    }
  },
  methods:{
    changeShow(){
      this.isCollapse = !this.isCollapse;
    }
  }
}
</script>

<style lang="less" scoped>
.layout{
  //display: flex;
  .menu{
    //width: 200px;
    background: #112f50;
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
  }
  .content{
    padding-left: 200px;
  }
  .small{
    padding-left: 64px;
    transition: padding-left 0s linear;
  }
}
</style>
<template>
  <div>
    <div class="header">
      <div class="open">
        <span v-if='!isCollapse' class="iconfont icon-right-indent" @click="changMenu"></span>
        <span v-if='isCollapse' class="iconfont icon-left-indent" @click="changMenu"></span>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  props:['isCollapse'],
  methods:{
    changMenu(){
      this.$emit('changeShow')
    }
  }
}
</script>

<style lang="less" scoped>
.header{
  height: 50px;
  background: #1e78bf;
  color: white;
  line-height: 50px;
  .open{
    .iconfont{
      font-size: 20px;
      cursor: pointer;
    }
  }
}
</style>
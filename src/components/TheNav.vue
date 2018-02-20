<template>
<div style="min-height: calc(100vh - 100px); background-color: #545c64">
  <el-menu class="el-menu-vertical-demo" :default-openeds="['1','2']" @open="handleOpen" @close="handleClose"
    background-color="#545c64" text-color="#fff" active-text-color="#409EFF">
    <el-submenu index="1">
      <template slot="title">
        <i class="el-icon-document"></i>
        <span>导航一</span>
      </template>
      <el-menu-item-group>
        <el-menu-item index="1-1">选项1</el-menu-item>
        <el-menu-item index="1-2">选项2</el-menu-item>
        <el-menu-item index="1-3">选项3</el-menu-item>
      </el-menu-item-group>
    </el-submenu>
    <el-submenu index="2">
      <template slot="title">
        <i class="el-icon-setting"></i>
        <span>导航二</span>
      </template>
      <el-menu-item-group>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
      </el-menu-item-group>
    </el-submenu>
  </el-menu>
</div>
</template>

<script>
export default {
  name: 'TheNav',
  methods: {
    handleOpen (key, keyPath) {
      console.log(key, keyPath)
    },
    handleClose (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style scoped lang="scss">
</style>

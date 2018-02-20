<template>
<el-container class="wrap">
  <el-header height="80px">
    <el-button icon="el-icon-tickets" @click="handleOpen"/>
    <the-header />
  </el-header>
  <el-container class="body-wrap">
    <el-aside width="200px" :class="{'open': open}">
      <the-nav />
    </el-aside>
    <el-container class="main-wrap">
      <el-main>Main</el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</el-container>
</template>

<script>
import TheHeader from '@/components/TheHeader'
import TheNav from '@/components/TheNav'
export default {
  name: 'home',
  data () {
    return {
      open: false
    }
  },
  components: {
    TheHeader,
    TheNav
  },
  methods: {
    handleOpen () {
      this.open = !this.open
      console.log(this.open)
    }
  }
}
</script>

<style scoped lang="scss">
@import '~@/common/css/base.scss';
.wrap {
  min-height: 96vh;
  .el-header {
    position: relative;
    background-color: #409EFF;
    line-height: 80px;
    .el-button {
      position: absolute;
      left: 10px;
      top: 50%;
      transform: translateY(-60%);
      border: #fff;
      background-color: #fff;
      @media screen and (min-width: $smallSize){
        display: none
      }
    }
  }
  .body-wrap {
    position: relative;
    overflow: hidden;
    .el-aside {
      background-color: #D3DCE6;
      color: #333;
      line-height: 200px;
      @include tran-horizontal(0, 0.4s);
      @media screen and (max-width: $smallSize) {
        position: absolute;
        left: -200px;
      };
      &.open {
        @include tran-horizontal(100%, 0.4s);
      }
    }
    .main-wrap {
      .el-main {
        background-color: #fff;
        color: #333;
        text-align: center;
        line-height: 160px;
      }
      .el-footer {
        color: #333;
        line-height: 70px;
        text-align: center;
        background-color: #D3DCE6;
      }
    }
  }
}
</style>

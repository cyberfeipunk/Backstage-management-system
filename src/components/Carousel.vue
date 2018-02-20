<template>
  <el-carousel :interval="4000" type="card" height="200px">
    <el-carousel-item v-for="(item, index) in items" :key="index" @Click="handleRouter(index)">
      <h3>{{item}}</h3>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: 'Carousel',
  props: {
    router: {
      type: Array
    },
    items: Array
  },
  methods: {
    handleRouter (i) {
      console.log(i)
      // this.$router.push(`${router[i]}`)
    }
  }
}
</script>

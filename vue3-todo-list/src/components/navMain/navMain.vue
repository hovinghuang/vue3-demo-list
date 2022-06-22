<template>
  <div class="main">
    <h1>一个人的信息</h1>
    <h2>姓名：{{msg}}</h2>
    <h2>年龄：{{name}}</h2>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  name: 'Main',
  props: ['msg', 'name'],
  setup(props, context) {
    console.log('---setup---props:', props)
    console.log('---setup---context:', context)

  }
}
</script>

<style scoped lang="scss">
.main {
  color: black;
}
</style>

<template>
  <div class="main">
    <h1>一个人的信息</h1>
    <h2>姓名：{{msg}}</h2>
    <h2>年龄：{{name}}</h2>
    <button @click="onEmitFunc">触发emit</button>

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
    console.log('---setup---context.attrs:', context.attrs)
    console.log('---setup---context.emit:', context.emit)
    console.log('---setup---context.expose:', context.expose)
    console.log('---setup---context.slots:', context.slots)

    const onEmitFunc = () => {
      context.emit('sayHello', 6666)
    }
    return {
      onEmitFunc
    }
  }
}
</script>

<style scoped lang="scss">
.main {
  color: black;
}
</style>

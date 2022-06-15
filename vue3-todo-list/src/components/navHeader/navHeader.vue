<template>
  <div class="header">
    <input placeholder="请输入任务名称" v-model="value" />
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'navHeader',
  props: {},
  setup() {}
})
</script>

<style scoped lang="scss">
.header {
    color: black;
}
</style>

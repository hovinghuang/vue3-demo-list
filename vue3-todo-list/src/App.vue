<template>
  <!-- <router-view/> -->
  <div>
    <button @click="isShowDemo = !isShowDemo">切换隐藏/显示</button>
    <Demo v-if="isShowDemo"></Demo>
    <hr>
    <Test></Test>
  </div>
</template>

<script>
import { ref } from 'vue'
import Demo from '@/components/hookDemo/Demo'
import Test from '@/components/hookDemo/Test'

export default {
  name: 'App',
  components: {
    Demo,
    Test
  },
  setup() {
    let isShowDemo = ref(true)
    return {
      isShowDemo
    }
  }
}
</script>


<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
</style>

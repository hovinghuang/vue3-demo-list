<template>
  <div class="home">
    <!-- <nav-header></nav-header>
    <nav-main></nav-main>
    <nav-footer></nav-footer> -->
    <div>{{num}}</div>
    <div>{{name}}</div>
  </div>
</template>

<script>
import NavHeader from '@/components/navHeader/navHeader.vue'
import NavMain from '@/components/navMain/navMain.vue'
import NavFooter from '@/components/navFooter/navFooter.vue'
import { defineComponent, ref, reactive, toRefs } from 'vue'

export default defineComponent({
  name: 'HomeView',
  components: {
    NavHeader,
    NavMain,
    NavFooter
  },
  props: {

  },
  setup(props, ctx) {
    // let num = ref(0)
    // let name = ref('jack')
    return {
      num,
      name
    }
  }
})
</script>

<style scoped lang="scss">
// .main {
//   color: black;
// }
</style>
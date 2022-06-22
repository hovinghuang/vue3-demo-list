<template>
  <div class="home">
    <!-- <nav-header></nav-header> -->
    <nav-main msg="你好啊" name="Vue3"></nav-main>
    <!-- <nav-footer></nav-footer> -->
    <!-- <div>名字: {{data.name}}</div>
    <div>年龄: {{data.age}}</div>
    <div>职业: {{data.job.type}}</div>
    <div>薪水: {{data.job.salary}}</div>
    <div>爱好: {{data.job.hobby}}</div> -->
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
    let data = reactive({
      name: '张三',
      age: 18,
      job: {
        type: '前端工程师',
        salary: '30k',
        a: {
          b: {
            c: 888
          }
        },
        hobby: ['学习', '运动', '看电影', '打球']
      }
    })
    // console.log("data:", data)
    data.job.salary = '60K'
    return {
      data
    }
  }
})
</script>

<style scoped lang="scss">
// .main {
//   color: black;
// }
</style>
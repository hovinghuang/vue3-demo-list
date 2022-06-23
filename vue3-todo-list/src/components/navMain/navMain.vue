<template>
  <div class="main">
    <h1>一个人的信息</h1>
    姓: <input type="text" v-model="data.firstName">
    <br>
    名: <input type="text" v-model="data.lastName">
    <br>
    全名：: <input type="text" v-model="data.fullName">
    <div>全名：{{data.fullName}}</div>
  </div>
</template>

<script>
import { reactive, computed } from 'vue'
export default {
  name: 'Main',
  // props: ['msg', 'name'],
  // computed: {
  //   fullName(){
  //     return this.data.firstName + this.data.lastName
  //   }
  // },
  setup(props, context) {
    const data = reactive({
      firstName: '张',
      lastName: '三',
      fullName: ''
    })

    // data.fullName = computed(() => {
    //   return data.firstName + '-' + data.lastName
    // })
    data.fullName = computed({
      get() {
        return data.firstName + '-' + data.lastName
      },
      set(value) {
        const nameArr = value.split('-')
        data.firstName = nameArr[0]
        data.lastName = nameArr[1]
      }
    })
    return {
      data
    }
  }
}
</script>

<style scoped lang="scss">
.main {
  color: black;
}
</style>

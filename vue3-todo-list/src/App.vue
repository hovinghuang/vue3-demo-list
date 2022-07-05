<!-- <template>
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
</style> -->

<template>
	<div class="app">
		<h3>我是App组件（祖），{{name}}--{{price}}</h3>
		<Child/>
	</div>
</template>

<script>
	import { reactive, toRefs, provide } from 'vue'
	import Child from './components/provide&inject/Child.vue'
	export default {
		name:'App',
		components:{ Child },
		setup(){
			let car = reactive({ name:'奔驰', price:'40W' })
			provide('car',car) // 给自己的后代组件传递数据
			return {...toRefs(car)}
		}
	}
</script>

<style>
	.app{
		background-color: gray;
		padding: 10px;
	}
</style>
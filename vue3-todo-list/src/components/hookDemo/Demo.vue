<template>
    <div>
        <h2>当前求和为：{{sum}}</h2>
        <button @click="sum++">点我+1</button>
        <hr>
        <h2>当前点击时鼠标的坐标为：x：{{point.x}}，y：{{point.y}}</h2>
    </div>
</template>

<script>
	import {
        ref,
        onBeforeMount,
        onMounted,
        onBeforeUpdate,
        onUpdated,
        onBeforeUnmount,
        onUnmounted
    } from 'vue'
	import usePoint from '@/hooks/usePoint'
	export default {
		name: 'Demo',
		setup() {
			// 数据
			let sum = ref(0)
			let point = usePoint()
			
            //通过组合式API的形式去使用生命周期钩子
			onBeforeMount(()=>{
				console.log('---onBeforeMount---')
			})
			onMounted(()=>{
				console.log('---onMounted---')
			})
			onBeforeUpdate(()=>{
				console.log('---onBeforeUpdate---')
			})
			onUpdated(()=>{
				console.log('---onUpdated---')
			})
			onBeforeUnmount(()=>{
				console.log('---onBeforeUnmount---')
			})
			onUnmounted(()=>{
				console.log('---onUnmounted---')
			})
            
			// 返回一个对象（常用）
			return { sum, point }
		},
        //通过配置项的形式使用生命周期钩子
		//#region 
		beforeCreate() {
			console.log('---beforeCreate---')
		},
		created() {
			console.log('---created---')
		},
		beforeMount() {
			console.log('---beforeMount---')
		},
		mounted() {
			console.log('---mounted---')
		},
		beforeUpdate(){
			console.log('---beforeUpdate---')
		},
		updated() {
			console.log('---updated---')
		},
		beforeUnmount() {
			console.log('---beforeUnmount---')
		},
		unmounted() {
			console.log('---unmounted---')
		},
		//#endregion
	}
</script>
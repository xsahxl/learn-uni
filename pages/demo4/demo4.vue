<template>
	<view>
		{{num}}
	</view>
	<view>{{num2}}</view>
	<view>{{str}}</view>
	<view>{{arr}}</view>
	<view>{{obj}}</view>
</template>

<script setup>
import { ref } from 'vue';
	let num = 1;
	// setInterval(()=>{
	// 	num++;
	// 	console.log(num)
	// }, 1000)
	
	let num2 = ref(10);
	setInterval(()=>{
		num2.value++;
		console.log(num2.value);
	}, 1000)
	let str = ref('测试');
	let arr = ref([1,2,3,4]);
	let obj = ref({name: 'xiaoming', age: 20});
	obj.value.name = 'xiaohong'
	
</script>

<style>

</style>

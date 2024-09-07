<template>
	<input type="text" v-model="firstName" placeholder="请输入姓"/>
	<input type="text" v-model="lastName" placeholder="请输入名" />
	<view class="">全部名称：{{fullName}}</view>
	<view class="">全部名称：{{fullName}}</view>
	<view class="">全部名称：{{fullName1()}}</view>
	<view class="">全部名称：{{fullName1()}}</view>
</template>

<script setup>
import { computed, ref } from 'vue';
	const firstName = ref('');
	const lastName = ref('');
	const fullName = computed(()=>{
		console.log('computed')
		return `${firstName.value}-${lastName.value}`
	})
	const fullName1 = ()=>{
		console.log('method')
		return `${firstName.value}-${lastName.value}`
	}
	
</script>

<style lang="scss" scoped>
	input{
		border: 1px solid #ccc;
	}

</style>


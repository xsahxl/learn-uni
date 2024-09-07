<template>
	<view class="box" @click="onClick">
		{{num}}
	</view>
	<view>
		<switch @change="onChange" />
		<button type="primary" :loading="isLoading">button</button>
	</view>
</template>

<script setup>
import { ref } from 'vue';
	let num = ref(0);
	let isLoading = ref(false)
	function onClick(){
		num.value++;
	}
	function onChange(e){
		isLoading.value = e.detail.value	
	}
	
</script>

<style>
	.box{
		width: 200px;
		height: 200px;
		background-color: red;
	}

</style>

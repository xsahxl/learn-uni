<template>
	<view>
		{{a}}
	</view>
	<view class="">
		{{Math.random()}}
	</view>
	<view class="">
		{{2+3}}
	</view>
	<view class="">
		{{fn()}}
	</view>
</template>

<script setup>
	const a = 6
	function fn(){
		return 'vue3 学习'
	}
</script>

<style>

</style>

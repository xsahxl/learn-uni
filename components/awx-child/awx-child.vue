<template>
	<view>
		子组件
		<!-- <button @click="$emit('add', 123)">按钮</button> -->
		<button @click="onAdd">button</button>
	</view>
</template>

<script setup>
	const emit = defineEmits(['add'])
	function onAdd(){
		emit('add', 123)
	}
</script>

<style>

</style>
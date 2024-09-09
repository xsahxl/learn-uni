<template>
	<view>
		子组件
		<!-- <button @click="$emit('add', 123)">按钮</button> -->
		<button @click="onAdd">button</button>
	</view>
</template>

<script setup>
import { onUnmounted } from 'vue';
const emit = defineEmits(['add'])
function onAdd(){
	emit('add', 123)
}
onUnmounted(()=>{
	console.log('组件被卸载了')
})
</script>

<style>

</style>
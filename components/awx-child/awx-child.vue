<template>
	<view>
		子组件
		<!-- <button @click="$emit('add', 123)">按钮</button> -->
		<button @click="onAdd">button</button>
	</view>
</template>

<script setup>
import { onUnmounted, ref } from 'vue';
const emit = defineEmits(['add'])
function onAdd(){
	emit('add', 123)
}
onUnmounted(()=>{
	console.log('组件被卸载了')
})
const count = ref(100);
defineExpose({
	count
})
</script>

<style>

</style>
<template>
	<view>
		<scroll-view scroll-y="true" ref='scroll' >
			<view>xx</view>
		</scroll-view>
		<awx-child v-if="show" @add="onAdd"></awx-child>
	</view>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue';
const scroll = ref(null);
console.log(scroll.value);
onMounted(()=>{
	console.log(scroll.value);
});
const show = ref(true);
function onAdd(){
	show.value = !show.value;
}
	
</script>

<style lang="scss" scoped>

</style>


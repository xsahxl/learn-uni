<template>
	<view>
		<scroll-view scroll-y="true" ref="scroll">
			<view>scroll</view>
		</scroll-view>
		<view>
			{{person.name}}
		</view>
		<navigator url="/pages/demo14/demo14">跳转demo14</navigator>
	</view>
</template>

<script setup>
import { onLoad, onReady, onShow } from '@dcloudio/uni-app';
import { ref } from 'vue';
const person = ref(null);
const scroll = ref(null)
onLoad((e)=>{
	console.log('onLoad', e);
	person.value = e;
	
})

onShow(()=>{
	console.log('onShow')
})

onReady(()=>{
	console.log('onReady', scroll.value)
})
	
</script>

<style lang="scss" scoped>

</style>


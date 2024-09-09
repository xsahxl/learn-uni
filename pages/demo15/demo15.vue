<template>
	<view>
		<scroll-view scroll-y="true" ref="scroll">
			<view>scroll</view>
		</scroll-view>
		<view>
			{{person.name}}
		</view>
		<navigator url="/pages/demo14/demo14">跳转demo14</navigator>
		<view class="">
			{{count}}
		</view>
	</view>
</template>

<script setup>
import { onLoad, onReady, onShow, onHide } from '@dcloudio/uni-app';
import { ref } from 'vue';
const person = ref(null);
const scroll = ref(null)

const count = ref(0);

let timer = setInterval(()=>{
	count.value++;
}, 100);

onLoad((e)=>{
	console.log('onLoad', e);
	person.value = e;
	
})

onShow(()=>{
	console.log('onShow', count.value)
	timer = setInterval(()=>{
		count.value++;
	}, 1000)
	
})

onHide(()=>{
	console.log('onHide', count.value)
	clearInterval(timer)
})

onReady(()=>{
	console.log('onReady', scroll.value)
})
	
</script>

<style lang="scss" scoped>

</style>


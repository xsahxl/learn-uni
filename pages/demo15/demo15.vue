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
		<navigator url="/pages/demo13/demo13" open-type="reLaunch">reLaunch demo14</navigator>
		<view v-for="(item,index) in 50" :key="index">
			{{item}}
		</view>
	</view>
</template>

<script setup>

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
	console.log('onHide', count.value);
	clearInterval(timer);
})

onBeforeMount(()=>{
	console.log('onBeforeMount');
})

onReady(()=>{
	console.log('onReady', scroll.value);
})

onMounted(()=>{
	console.log('onMounted');
})

onUnload(()=>{
	console.log('onUnload组件卸载了');
})

onPageScroll((e)=>{
	console.log('onPageScroll', e)
})


	
</script>

<style lang="scss" scoped>

</style>


<template>
	<view>
		<image :src="picture" mode=""></image>
		<button type="primary" :loading="false">按钮</button>
		
	</view>
</template>

<script setup>
import { ref } from 'vue';
	const list = ref([
		'../../static/pic1.png',
		'../../static/pic2.png',
		'../../static/pic4.jpg',
		'../../static/pic3.webp'
	]);
	const picture = ref(list.value[0]);
	
	let i = 0;
	setInterval(()=>{
		i++;
		if(i===4) i=0;
		picture.value = list.value[i];
	}, 1000)
</script>

<style>

</style>

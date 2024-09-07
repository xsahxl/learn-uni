<template>
	<view>
		<image :src="picture" mode=""></image>
		<button type="primary" :loading="false">按钮</button>
		<view class="box" :class="{active: isActive}">
			class测试
		</view>
		<view class="box" :class="0 ? 'active': ''">
			class测试
		</view>
		<view class="box" :style="{width: '300px'}">
			style测试
		</view>
		
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
	const isActive = ref(false);
	
	let i = 0;
	setInterval(()=>{
		i++;
		if(i===4) i=0;
		picture.value = list.value[i];
		isActive.value = !isActive.value;
	}, 1000)
</script>

<style>
	.box{
		width: 200px;
		height: 200px;
		background-color: red;
	}
	.active{
		background-color: yellow;
	}

</style>

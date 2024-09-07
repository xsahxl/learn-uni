<template>
	<view v-if="shop">淘宝</view>
	<view v-else>京东</view>
	
	<view v-if="day===1">星期一</view>
	<view v-else-if="day===2">星期二</view>
	<view v-else>星期三</view>
	<view class="box1" v-if="false">v-if</view>
	<view class="box2" v-show="false">v-show</view>
	
	<view class="box3">
		box3
	</view>
	<template v-if="true">
		<view class="">
			box4
		</view>
		<image src="../../static/pic1.png" mode=""></image>
	</template>
	
</template>

<script setup>
import { ref } from 'vue';
const day = ref(2)
	
</script>

<style lang="scss" scoped>

</style>


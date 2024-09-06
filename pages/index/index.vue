<template>
	<view class="box" hover-class="boxHover">
		<view class="inner" hover-class="innerHover" hover-stop-propagation>
			内部元素
		</view>
	</view>
	<view class="">-----</view>
	<text selectable space="emsp ">text    标签</text>
	<scroll-view scroll-x class="scrollView">
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		<view class="box">子元素</view>
		
	</scroll-view>

</template>

<script setup>
	
</script>

<style lang="scss">
	.scrollView{
		width: 80%;
		height: 200px;
		border: 1px solid red;
		white-space: nowrap;
		.box{
			width: 100px;
			height: 100px;
			background-color: green; 
			display: inline-block;
			margin: 8px;
		}
	}
	
</style>

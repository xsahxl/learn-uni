<template>
	<view class="header">
		<slot name='header'>
			header默认内容
		</slot>
	</view>
	<view class="main">
		<slot></slot>
	</view>
	<view class="footer">
		footer
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.header{
		background-color: red;
	}
	.main{
		height: 200px;
		background-color: pink;
	}
	.footer{
		background-color: yellow;
	}

</style>
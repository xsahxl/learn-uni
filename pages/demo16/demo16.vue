<template>
	<view>demo16</view>
	<button @click="show" >show</button>
	<button @click="hide" >hide</button>
</template>

<script setup>
function show(){
	uni.showToast({
		title:'操作成功',
		duration:2000
	})
}

function hide(){
	uni.hideToast()
}
	
</script>

<style lang="scss" scoped>

</style>


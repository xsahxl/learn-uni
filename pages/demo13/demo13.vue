<template>
	<view>
		<awx-child @add="onAdd"></awx-child>
	</view>
</template>

<script setup>
	function onAdd(v){
		console.log(v)
	}
	
</script>

<style lang="scss" scoped>

</style>


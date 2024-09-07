<template>
	<view class="item" v-for="item in goods" :key="item.id">
		<checkbox></checkbox>
		<view class="title">
			{{item.name}}
		</view>
		<view class="delete" @click="remove(item.id)">
			删除
		</view>
	</view>
</template>

<script setup>
import { ref } from 'vue';
const goods = ref([
	{id: 1, name: '小米'},
	{id: 2, name: '华为'},
	{id: 3, name: 'oppo'},
	{id: 4, name: '苹果'}
]);

function remove(id){
	console.log(id)
	goods.value = goods.value.filter(o=>o.id !== id)
}
</script>

<style lang="scss" scoped>
.item{
	display: flex;
	align-items: center;
	padding: 4px 16px;
	.delete{
		color: red;
		margin-left: 30px;
	}
}
</style>


<template>
	<checkbox-group @change="checkboxChange">
		<view class="item" v-for="item in goods" :key="item.id">
		<checkbox :value="item.id" :checked="item.checked"></checkbox>
		<view class="title">
			{{item.name}}
		</view>
		<view class="price">
			{{item.price}}元
		</view>
		<view class="delete" @click="remove(item.id)">
			删除
		</view>
	</view>
	</checkbox-group>
	<view class="footer">
		选中{{ selected.length }}个，共{{totalMoney}}元
	</view>
	{{ goods }}
</template>

<script setup>
import { ref, computed } from 'vue';
const goods = ref([
	{id: '1', name: '小米', price: 1999, checked: false},
	{id: '2', name: '华为', price: 2999, checked: false},
	{id: '3', name: 'oppo', price: 3999, checked: false},
	{id: '4', name: '苹果', price: 4999, checked: false}
]);

function remove(id){
	console.log(id)
	goods.value = goods.value.filter(o=>o.id !== id)
}

const selected = ref([]);
const totalMoney = computed(()=>goods.value.filter(o=>o.checked).reduce((a,b)=>a+b.price,0))

function checkboxChange(e){
	selected.value = e.detail.value;
	goods.value = goods.value.map(o=>({...o, checked: selected.value.includes(o.id)}))
}
</script>

<style lang="scss" scoped>
.item{
	display: flex;
	align-items: center;
	padding: 4px 16px;
	.price{
		margin-left: 30px;
	}
	.delete{
		color: red;
		margin-left: 30px;
	}
}
.footer{
	margin-top: 16px;
	border-top: 1px solid #000;
	padding: 16px;
}
</style>


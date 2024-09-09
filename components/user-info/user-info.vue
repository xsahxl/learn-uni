<template>
	<view>
		{{username}}
	</view>
</template>

<script setup>
// import { computed, ref } from 'vue';
// const props = defineProps(['username'])
// const name = computed(()=>props.username+'7')
defineProps({
	username:{
		type: String,
		// default: '匿名' 
		default(){
			return '匿名'; 
		}
	}
});
</script>

<style>

</style>
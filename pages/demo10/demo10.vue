<template>
	<view>
		<input type="text" v-model="count" />
		<input type="text" v-model="person.name" />
	</view>
</template>

<script setup>
import { ref, watch, watchEffect } from 'vue';
	const count = ref(0);
	watch(count, newVal=>{
		console.log('count', newVal);
	})
	const person = ref({name: '小明', age: 20});
	watch(()=>person.value.name, (newVal)=>{
		console.log('person.name', newVal)
	})
	
	watch(person, newVal=>{
		console.log('person', newVal)
	}, {
		deep: true,
		immediate: true
	})
	watchEffect(()=>{
		console.log('watchEffect1' ,count.value)
	})
	watchEffect(()=>{
		console.log('watchEffect2' ,person.value.name)
	})
	
	
</script>

<style lang="scss" scoped>

</style>


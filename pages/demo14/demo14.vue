<template>
	<view>
		<scroll-view scroll-y="true" ref='scroll' >
			<view>xx</view>
		</scroll-view>
		<awx-child v-if="show" @add="onAdd" ref="child"></awx-child>
	</view>
	<navigator url="/pages/demo15/demo15?name=xiaoming&age=20">跳转到demo15 </navigator>
</template>

<script setup>
import { onMounted, ref } from 'vue';
const scroll = ref(null);
onMounted(()=>{
	console.log('scroll.value', scroll.value);

});
const show = ref(true);
function onAdd(){
	show.value = !show.value;
}

const child = ref(null);
onMounted(()=>{
	console.log('child.value', child.value.count);
})
</script>

<style lang="scss" scoped>

</style>


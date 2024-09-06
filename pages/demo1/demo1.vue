<template>
	<view>
		<swiper indicator-dots indicator-color="#007aff" indicator-active-color="#4cd964" circular autoplay>
			<swiper-item>
				<view class="swiper-item">111</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">2222</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">3333</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">4444</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss">
	   swiper{
		   width: 100vw;
		   height: 200px;
		   border: 1px solid red;
		   swiper-item{
			   width: 100%;
			   height: 100%;
			   background-color: pink;
		   }
		   swiper-item:nth-child(2n){ 
			   background-color: orange;
		   }
	   }    
</style>
 
<template>
	
		<view>
			<swiper indicator-dots indicator-color="#007aff" indicator-active-color="#4cd964" circular autoplay vertical>
				<swiper-item>
					<image src="../../static/pic1.png" mode="aspectFill"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/pic2.png" mode="aspectFit"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/pic4.jpg" mode="aspectFill"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/pic3.webp" mode="aspectFit"></image>
				</swiper-item>
			</swiper>
		</view>
		<image class="picture" src="../../static/logo.png" mode=""></image>
		<image class="picture" src="../../static/pic1.png" mode="aspectFill"></image>
		<image class="picture" src="../../static/pic2.png" mode=""></image>
		<image class="picture" src="../../static/pic4.jpg" mode=""></image>
		<image src="../../static/pic3.webp" mode="aspectFill"></image>
		<image src="https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/uni-app.png" mode="aspectFit"></image>
	
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
			   image{
				   width: 100%;
				   height: 100%;
			   }
		   }
		   swiper-item:nth-child(2n){ 
			   background-color: orange;
		   }
	   }    
	   .picture{
		   width: 150px;
		   height: 150px;
	   }
</style>
 
<template>
	<view>demo16</view>
	<button @click="showToast" >showToast</button>
	<button @click="hideToast" >hideToast</button>
	<button @click="showLoading" >showLoading</button>
	<button @click="hideLoading" >hideLoading</button>
	<button @click="showModal" >showModal</button>
	<button @click="showActionSheet" >showActionSheet</button>
</template>

<script setup>
function showToast(){
	uni.showToast({
		title:'操作成功',
		duration:2000
	});
}

function hideToast(){
	uni.hideToast();
}

function showLoading(){
	uni.showLoading({
		title: "加载中..."
	});
}

function hideLoading(){
	uni.hideLoading();
}

function showModal(){
	uni.showModal({
		title: "删除",
		content: "您确定要删除该数据么？",
		cancelText: "NO",
		confirmText: "YES",
		// editable: true,
		// placeholderText: "请输入xx",
		success: (e) => {
			console.log(e)
		}
	})
}

function showActionSheet(){
	uni.showActionSheet({
		itemList: ['A', 'B', 'C'],
		success: function (res) {
			console.log('选中了第' + (res.tapIndex + 1) + '个按钮');
		},
		fail: function (res) {
			console.log(res.errMsg);
		}
	});

}
	
</script>

<style lang="scss" scoped>

</style>


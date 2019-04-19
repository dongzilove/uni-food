<template>
	<view class="content">
	    <image class="logo" src="/static/img/logo.png"></image>
		<view>
	        <text class="title">{{titles}}</text>
	    </view>
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue";
	export default{
		data(){
			return{
				titles:"我是热门"
			}
		},
		components: {uniGrid},
	}
</script>

<style>
	.content {
	text-align: center;
	height: 400upx;
	margin-top: 200upx;
	}
	.logo{
	    height: 200upx;
	    width: 200upx;
	    margin-top: 200upx;
	}
	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>

<template>
	<view class="content">
		<uni-grid :options="[
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/shu.png',text:'圣诞树'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/lindang.png',text:'铃铛'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/laoren.png',text:'圣诞老人'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/liwu.png',text:'礼物'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/maozi.png',text:'帽子'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/shoutao.png',text:'手套'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/xueqiao.png',text:'雪橇'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/xunlu.png',text:'驯鹿'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/xuehua.png',text:'雪花'}]">
		</uni-grid>
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

<template>
	<view>
		<view class="my-plan-style">
			<!-- 3D轮播 -->
			<view class="">
				<swiper class="imageContainer" previous-margin="50rpx" next-margin="50rpx" circular  autoplay>
					<block v-for="(item,index) in imgList" :key="index">
						<swiper-item class="swiperitem">
							<image class="itemImg" :class="currentIndex == index ? 'swiperactive': ''" :src="item" lazy-load mode="scaleToFill"></image>
						</swiper-item>
					</block>
				</swiper>
			</view>
		</view>
        <image class="logo" src="/static/img/logo.png"></image>
		<view>
            <text class="title">{{title}}</text>
        </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				imgList:[
					'../../static/img/swiper/timg1.jpg',
					'../../static/img/swiper/timg2.jpg',
					'../../static/img/swiper/timg3.jpg',
					'../../static/img/swiper/timg4.jpg',]
				}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
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
	.imageContainer {
		width: 100%;
		height: 325upx;
		background-color: #fff;
	}
	
	.swiperitem {
		height: 255upx;
		padding: 0upx 20upx;
		box-sizing: border-box;
		position: relative;
		
		.swiperText{
			
			display: flex;
			flex-direction: column;
			align-items: center;
			position: absolute;
			top: 56upx;
			left: 51upx;
			z-index: 998;
			width:162upx;
			height:163upx;
			background:rgba(255,255,255,1);
			border-radius:8upx;
			padding:10upx;
			
			.name {
				font-size:26upx;
				font-weight:500;
				color:rgba(253,57,91,1);
				line-height:37upx;
				margin-bottom: 10upx;
			}
			.zq,.cz {
				font-size:20upx;
				color:rgba(253,57,91,1);
				line-height:35upx;
			}
			.addNl {
				width:120upx;
				height:26upx;
				background:rgba(253,57,91,1);
				border-radius:13upx;
				font-size:20upx;
				font-weight:500;
				color:rgba(255,255,255,1);
				text-align: center;
				line-height: 26upx;
				margin-top: 10upx;
			}
			
		}
	}
	
	.itemImg {
		position: absolute;
		width: 95%;
		/* height: 380rpx; */
		height: 255upx;
		border-radius: 15rpx;
		z-index: 5;
		opacity: 0.7;
		top: 5%;
		box-shadow:0px 4upx 15upx 0px rgba(153,153,153,0.24);
	}
	
	.swiperactive {
		width: 95%;
		opacity: 1;
		z-index: 10;
		/* height: 430rpx; */
		height: 287upx;
		top: 0%;
		transition: all .2s ease-in 0s;
	}
	
	.zhankai{
		text-align: center;
		.iconfont{
			margin-left: 10upx;
		}
	}
</style>

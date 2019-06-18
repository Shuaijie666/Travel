<template>
	<view class="percen">
		<view>
			<!-- 图标 -->
			<view class="top-one">
				<uni-icon type="gear" size="24"></uni-icon>
				<uni-icon type="scan" size="22"></uni-icon>
				<uni-icon class="right" type="chat" size="22"></uni-icon>
			</view>
			<!-- 头部 -->
			<view class="top-two">
				<view class="welcome">
					Hi~欢迎来到马蜂窝
				</view>
				<view class="wish">
					愿每一个旅行愿望得以达成
				</view>
				<!-- 登陆注册按钮 -->
				<view class="le">
					<view class="le-one" @click="login">登陆</view>
					<view class="le-two">/</view>
					<view class="le-three"  @click="register">注册</view>
				</view>
				<!-- 动态图 -->
				<view class="gif" ></view>
			</view>
			<!-- 横向布局 -->
			 <view class="box">
			 	<view class="box-bd">
			 		<view class="item">
			 			<view class="icon"><img src="../../static/img/sc.png"></view>
			 			<view class="text">我的通知</view>
			 		</view>
			 		<view class="item">
			 			<view class="icon"><img src="../../static/img/4.png"></view>
			 			<view class="text">我的收藏</view>
			 		</view>
			 		<view class="item" >
			 			<view class="icon"><img src="../../static/img/ls.png"></view>
			 			<view class="text">我的客服</view>
			 		</view>
			 	</view>
			 </view>
			 <!-- 每日领蜂蜜 -->
			 <view class="neck">
			 	<view class="neck-a"></view>
			 	<view class="neck-b">
					<view class="neck-b-a">免费领取蜂蜜</view>
					<view class="neck-b-b">领取蜂蜜可用于消费抵现哦</view>
				</view>
			 	<view class="neck-c">
					<view class="neck-c-a">
						去领取
					</view>
				</view>
			 </view>
			 <!-- 我的足迹 -->
			 <view class="spoor">
			 	<view class="spoor-left">
					<view class="spoor-left-a">我的足迹</view>
					<view class="spoor-left-b">点击生成我的足迹地图</view>
				</view>
			 	<view class="spoor-right">
					<uni-icon type="forward" color="white" size="23"></uni-icon>
				</view>
			 </view>
			 <!-- 我的旅行 -->
			 <view class="travel">
			 	<view class="travel-top">我的旅行</view>
			 	<view class="travel-center">
					<view class="travel-center-one">+</view>
					<view class="travel-center-two">上传照片</view>
				</view>
			 	<view class="travel-bottom">
					如何用照片记录旅行？
				</view>
			 </view>
			 <!-- 更多服务 -->
			 <view class="serve">
				 <view class="serve-top">更多服务</view>
			 	<uni-grid :options='options'  :show-border="false" column-num='4'></uni-grid>
			 </view>
		</view>
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	export default {
		components:{
			uniGrid,
			uniIcon
		},
		data() {
			return {
				options:[
					{image:'../../static/img/wdqb.png',text:'我的钱包'},
					{image:'../../static/img/yh.png',text:'优惠券'},
					{image:'../../static/img/wdhd.png',text:'我的活动'},
					{image:'../../static/img/xz.png',text:'我的小组'},
					{image:'../../static/img/wdhy.png',text:'我的会员'},
					{image:'../../static/img/wdfm.png',text:'我的蜂蜜'},
					{image:'../../static/img/lxzb.png',text:'旅行装备'},
					{image:'../../static/img/cjaq.png',text:'出境安全'},
					{image:'../../static/img/yqyl.png',text:'邀请有礼'}]
				}
		},
		methods: {
			login(){
				uni.navigateTo({
					url: 'login'
				});
			},
			register(){
				uni.navigateTo({
					url: 'register'
				});
			}
			
		}
	}
</script>

<style lang="scss">
	@import url("../../static/css/percrn.css");
	.box{
		width: 90%;
		height: 180upx;
		border-radius: 20upx;
		position: relative;
		top: -3px;
		margin: 0 auto;
		background: #fff;
		// box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .0); 
		.box-bd{
			display: flex;
			flex-wrap: nowrap;
			flex-direction: row;
			justify-content: center;
			.item{
				flex: 1 1 auto;
				display: flex;
				flex-wrap: wrap;
				flex-direction: row;
				justify-content: center;
				border-right: 1px solid #f1f1f1;
				margin: 25upx 0;
				&:last-child{
					border: none;
				}
				.icon{
					width: 60upx;
					height: 60upx;
					img{
						width: 100%;
						height: 100%;
					}
				}
				.text{
					width: 100%;
					text-align: center;
					margin-top: 25upx;
					font-size: 13px;
				}
			}
		}
	}
</style>

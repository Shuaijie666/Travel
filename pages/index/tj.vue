<template>
	<view class="content">
		<view>
			 <view class="z-text">热门精选</view>
			 
			 <view class="scroll_box"> 
				<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
				  <view class="item_a" >
						<image src="../../static/home/l1.jpg" class="item_book_img" mode="aspectFill"></image>
				  </view>
				  <view class="item_b" >
						<image src="../../static/home/l2.jpg" class="item_book_img1" mode="aspectFill"></image>
				  </view>
				  <view class="item_c">
						<image src="../../static/home/l3.jpg" class="item_book_img2" mode="aspectFill"></image>
				  </view>
				 <view class="item_d">
						<image src="../../static/home/l4.jpg" class="item_book_img3" mode="aspectFill"></image>
				  </view>
				  <view class="item_e">
						<image src="../../static/home/l5.jpg" class="item_book_img4" mode="aspectFill"></image>
				  </view>
				  <view class="item_f"></view>
				</scroll-view>
			   </view>
		</view>
		<view class="tes">
			<view class="te1">好店好货</view>
			<view class="te2">蜜月圣地---马尔代夫</view>
			<view class="te3">蜜月必选,在最美的地方记录最美的你</view>
			<view class="tu">
				<image src="../../static/img/lx/my.jpg"></image>
			</view>
		</view>
		<view class="grids">
			<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='2'></uni-grid>
		</view>
		<!-- <view class="loading-text">我是有底线的.....</view> -->
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	export default {
		components: {uniGrid},
		data() {
			return {
			oppo:[
				{image:'../../static/home/goods/t1.jpg',text:'蛇口价值工厂/免费/涂鸦/废弃style'},
				{image:'../../static/home/goods/t2.jpg',text:'旅游不在乎终点 而是在意途中的人和事'},
				{image:'../../static/home/goods/t3.jpg',text:'伯纳乌球场-马德里'},
				{image:'../../static/home/goods/t4.jpg',text:'伯纳乌球场-马德里'},
				{image:'../../static/home/goods/t5.jpg',text:'停下奔波的脚步，体会自然'},
				{image:'../../static/home/goods/t6.jpg',text:'游船下午茶 杭州西溪悦榕庄'},
				{image:'../../static/home/goods/t7.jpg',text:'宁夏周边去哪玩'},
				{image:'../../static/home/goods/t8.jpg',text:'雷阿尔城 柏莱多'},
				{image:'../../static/home/goods/t9.jpg',text:'红砖美术馆  北京'},
				{image:'../../static/home/goods/t10.jpg',text:'旅游不在乎终点'},
				]
			};
		},
		mounted() {
			
		},
		methods:{
			
		}
	}
</script>

<style>
	.loading-text {
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 60upx;
		color: #979797;
		font-size: 38upx;
		/* border: #000000 1px solid; */
	}
	.scroll_box{ 
		width: 95%;height: 240upx;overflow: hidden;padding: 20rpx;background: #fff;white-space: nowrap;}
	.item_a,.item_b,.item_c,.item_d,.item_e,.item_f{width: 180rpx;height: auto;margin-right: 10rpx;display: inline-block;}
	.item_book_img{width: 300upx;height: 110px;border-radius: 5px;}
	.item_book_img1{width: 300upx;height: 110px;border-radius: 5px;margin-left: 120upx;}
	.item_book_img2{width: 300upx;height: 110px;border-radius: 5px;margin-left: 240upx;}
	.item_book_img3{width: 300upx;height: 110px;border-radius: 5px;margin-left: 360upx;}
	.item_book_img4{width: 300upx;height: 110px;border-radius: 5px;margin-left: 480upx;}
	
	.z-text{
		font-size: 40upx;
		font-weight: bold;
		margin-left: 10upx;
	}
	.tes{
		
		margin-top: 10upx;
	}
	.te1{
		font-size: 30upx;
		font-weight: bold;
		color:red;
	}
	.te2{
		margin-top: 20upx;
		font-size: 40upx;
		font-weight: bold;
		
	}
	.te3{
		color: #979797;
		font-size: 28upx;
		margin-top: 10upx;
	}
	
	.grids{
		margin-top: 20upx;
		height: 1850upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		/* border: #000000 1px solid; */
	}
	
	.grids .uni-grid{
		padding-left: 0upx;
		padding-top: -5upx;
		/* height: 150px; */
		/* margin: -30px 0upx; */
	    /* border: #000000 1px solid; */
		/* margin-top: 20upx; */
		
	}
	
	
	.grids .uni-grid image{
		height: 260upx;
		width: 350upx;
		border-radius: 10upx;
	}
	.grids .uni-grid text{
		font-size: 30upx;
		margin-top: 10upx;
		font-weight: bold;
	}
/* 	.content {
		margin-top: 50upx;
		text-align: center;
		height: 400upx;
	}

	.title {
		font-size: 36upx;
	} */
</style>

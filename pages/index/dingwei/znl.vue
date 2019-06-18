<template>
	<view class="content">
		<!-- <view class="titles">
			旅游攻略
		</view> -->
		<view class="grid">
			<uni-grid class="uni-grid" :options='option'  :show-border="false" column-num='3'></uni-grid>
		</view>
		
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
			<view class="grids">
			<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='2'></uni-grid>
		</view>
		
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	export default {
		components: {uniGrid},
		data() {
			return {
			option:[
			{image:'../../static/img/home/lbj.jpg',text:'北京周边去哪'},
			{image:'../../static/img/home/gg.jpg',text:'假装在国外'},
			{image:'../../static/img/home/cc.jpg',text:'网红拍照地'},
			{image:'../../static/img/home/lbj.jpg',text:'北京周边去哪'},
			{image:'../../static/img/home/gg.jpg',text:'假装在国外'},
			{image:'../../static/img/home/cc.jpg',text:'网红拍照地'}
			],
			oppo:[
			{image:'../../static/home/goods/t1.jpg',text:'蛇口价值工厂/免费/涂鸦/废弃style'},
			{image:'../../static/home/goods/t2.jpg',text:'旅游不在乎终点 而是在意途中的人和事'},
			{image:'../../static/home/goods/t3.jpg',text:'伯纳乌球场-马德里'},
			{image:'../../static/home/goods/t4.jpg',text:'伯纳乌球场-马德里'},
			{image:'../../static/home/goods/t5.jpg',text:'停下奔波的脚步，体会自然'},
			{image:'../../static/home/goods/t6.jpg',text:'游船下午茶 杭州西溪悦榕庄'},
			{image:'../../static/home/goods/t7.jpg',text:'宁夏周边去哪玩'},
			{image:'../../static/home/goods/t8.jpg',text:'雷阿尔城 柏莱多'},
			/* {image:'../../static/home/goods/t9.jpg',text:'红砖美术馆  北京'},
			{image:'../../static/home/goods/t10.jpg',text:'旅游不在乎终点'}, */
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
	/* .content {
		margin-top: 50upx;
		text-align: center;
		height: 400upx;
	}

	.title {
		font-size: 36upx;
	} */
	
	.titles {
			font-size: 50upx;
			text-align: center;
			margin-top: 15upx;
		}
		.grid{
			margin-top: 20upx;
			height: 500upx;
			width: 100%;
			border-radius: 10upx;
			margin-left: 0upx;
			/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
			/* border: #000000 1px solid; */
		}
		.grid .uni-grid{
			padding-left: 0upx;
			padding-top: -5upx;
			/* height: 150px; */
			/* margin: -30px 0upx; */
		    /* border: #000000 1px solid; */
			/* margin-top: 20upx; */
			
		}
		
		.grid .uni-grid image{
			height: 150upx;
			width: 200upx;
			border-radius: 10upx;
		}
		.grid .uni-grid text{
			font-size: 30upx;
			margin-top: 10upx;
			font-weight: bold;
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
		.grids{
			margin-top: 20upx;
			height: 1200upx;
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
			height: 350upx;
			width: 350upx;
			border-radius: 10upx;
		}
		.grids .uni-grid text{
			font-size: 30upx;
			margin-top: 10upx;
			font-weight: bold;
		}
</style>

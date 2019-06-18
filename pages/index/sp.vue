<template>
	<view class="content">
			<view class="tes">
				<view class="te1">好店好货</view>
				<view class="te2">女神归来--------张敏 横店见面会</view>
				<view class="te3">明星见面会邀你共同参与</view>
				<view class="tu">
					<image src="../../static/img/lx/ns.jpg"></image>
				</view>
			</view>
			
			  <view class="zt" >
				 <view class="v1">
					 <view style="font-size: 36upx; color: #000000; font-weight: bold;">【曼谷酒店】高逼格无边游泳池就在这里</view>
					 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">避开人人从纵仆，无边游泳池任你拍拍拍。</view>
				 </view>
				 
				 <view class="v2">
					 <image src="../../static/img/jd/jd4.jpg"></image>
					 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
				 </view>
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
			oppo:[
				{image:'../../static/home/goods/t1.jpg',text:'蛇口价值工厂/免费/涂鸦/废弃style'},
				{image:'../../static/home/goods/t2.jpg',text:'旅游不在乎终点 而是在意途中的人和事'},
				{image:'../../static/home/goods/t3.jpg',text:'伯纳乌球场-马德里'},
				{image:'../../static/home/goods/t4.jpg',text:'伯纳乌球场-马德里'},
				{image:'../../static/home/goods/t5.jpg',text:'停下奔波的脚步，体会自然'},
				{image:'../../static/home/goods/t6.jpg',text:'游船下午茶 杭州西溪悦榕庄'},
				{image:'../../static/home/goods/t7.jpg',text:'宁夏周边去哪玩'},
				{image:'../../static/home/goods/t8.jpg',text:'雷阿尔城 柏莱多'},
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
	
		.scroll_box{ 
		width: 95%;height: 240upx;overflow: hidden;padding: 20rpx;background: #fff;white-space: nowrap;}
	.item_a,.item_b,.item_c,.item_d,.item_e,.item_f{width: 180rpx;height: auto;margin-right: 10rpx;display: inline-block;}
	.item_book_img{width: 300upx;height: 110px;border-radius: 5px;}
	.item_book_img1{width: 300upx;height: 110px;border-radius: 5px;margin-left: 120upx;}
	.item_book_img2{width: 300upx;height: 110px;border-radius: 5px;margin-left: 240upx;}
	.item_book_img3{width: 300upx;height: 110px;border-radius: 5px;margin-left: 360upx;}
	.item_book_img4{width: 300upx;height: 110px;border-radius: 5px;margin-left: 480upx;}
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
	.v1{
		/* border: #000000 1px solid; */
		height: 100%;
		width: 47%;
		float: left;
		/* margin-top: -80upx; */
	}
	
	.v1{
		/* border: #000000 1px solid; */
		height: 100%;
		width: 47%;
		float: left;
		/* margin-top: -80upx; */
	}
	.v2{
		/* border: #000000 1px solid; */
		height: 100%;
		width: 49%;
		display: inline-block;
		float: right;
	}
	.v2 image{
		height: 200upx;
		width: 370upx;
		/* border-radius: 5px; */
	}
	.zt{
		margin-top: 10upx;
		width: 100%;
		height: 300upx;
		/* border: #000000 1px solid; */
	}
	
	.grids{
		margin-top: 20upx;
		height: 1000upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		border: #000000 1px solid;
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

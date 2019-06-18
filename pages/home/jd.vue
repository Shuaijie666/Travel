<template>
	<view class="content">
		
	<view>
	   <swiper class="carousel" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="duration" indicator-color="#FFF">
			<swiper-item>
				<image src="../../static/img/jd/lb1.png" class="sw-img"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/img/jd/lb2.png" class="sw-img"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/img/jd/lb3.png" class="sw-img"></image>
			</swiper-item>
		</swiper>
	</view>
	<!-- 搜索框 -->
	<view class="sousuo">
		<view class="ss">
			<image src="../../static/img/ss.png" style="width: 50upx; height: 50upx;"></image>
		</view>
		<input placeholder="搜索目的地/酒店" style="font-weight: bold; color:black; font-size: 35upx;"/>
	</view>
	
	 <view>
	 	<view class="grids">
	 		<uni-grid :options='options'  :show-border="false" column-num='5'></uni-grid>
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
	 <view class="te">
	 	<view  class="z-text">曼谷怎么玩</view>
	 	<view class="grid">
	 		<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='3'></uni-grid>
	 	</view>
	 	
	 </view>
	  <view class="z-text">
	 		 推荐
	 </view>
	 <view class="zt" >
		 <view class="v1">
			 <view style="font-size: 40upx; color: #000000; font-weight: bold;">【年度民宿榜】境外10大走心民宿</view>
			 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">马蜂窝酒店2018年榜单来袭！</view>
		 </view>
		 
		 <view class="v2">
			 <image src="../../static/img/jd/jd1.jpg"></image>
			 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
		 </view>
	 </view>
	  <view class="zt" >
	 		 <view class="v1">
	 			 <view style="font-size: 36upx; color: #000000; font-weight: bold;">【年度颜值榜】全球10大无边游泳池店,你想跳进哪一个？</view>
	 			 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">马蜂窝酒店2018年榜单来袭！</view>
	 		 </view>
	 		 
	 		 <view class="v2">
	 			 <image src="../../static/img/jd/jd2.jpg"></image>
	 			 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
	 		 </view>
	 </view>
	   <view class="zt" >
	 		 <view class="v1">
	 			 <view style="font-size: 36upx; color: #000000; font-weight: bold;">【干货】出国订酒店疑难杂症大解密</view>
	 			 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">出国酒店经常弄不明白的问题，一次说个清楚！</view>
	 		 </view>
	 		 
	 		 <view class="v2">
	 			 <image src="../../static/img/jd/jd3.jpg"></image>
	 			 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
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
	 
	  <view class="zt" >
	 		 <view class="v1">
	 			 <view style="font-size: 36upx; color: #000000; font-weight: bold;">【曼谷一日游】来曼谷住这些酒店就对了！</view>
	 			 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">曼谷怎么住？，看这篇就知道了。</view>
	 		 </view>
	 		 
	 		 <view class="v2">
	 			 <image src="../../static/img/jd/jd5.jpg"></image>
	 			 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
	 		 </view>
	 </view>
	   <view class="zt" >
	 		 <view class="v1">
	 			 <view style="font-size: 36upx; color: #000000; font-weight: bold;">曼谷除了美食还有必体验的网红酒店</view>
	 			 <view style="color: #979797;font-size: 38upx; margin-top: 20upx;">资深达人分享,曼谷网红的7大酒店。</view>
	 		 </view>
	 		 
	 		 <view class="v2">
	 			 <image src="../../static/img/jd/jd6.jpg"></image>
	 			 <view style="color: #979797;font-size: 38upx;">4930阅读 1357收藏</view>
	 		 </view>
	 </view>
	 
	 <view class="loading-text">我是有底线的.....</view>
	 
	 
	 
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	export default {
		components: {uniGrid},
		data() {
			return {
				options:[
				{image:'../../static/img/y14.jpg'},
				{image:'../../static/img/y1.jpg'},
				{image:'../../static/img/y2.jpg'},
				{image:'../../static/img/y3.jpg'},
				{image:'../../static/img/y4.jpg'}
				],
				oppo:[
				{image:'../../static/home/goods/t1.jpg'},
				{image:'../../static/home/goods/t2.jpg'},
				{image:'../../static/home/goods/t3.jpg'},
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
	.carousel{
		width: 100%;
		height: 340upx;
	}
	.sw-img{
		width: 750upx;
		height: 340upx;
	}
	.sousuo{
		width: 80%;
		height: 60upx;
		background-color: white;
		border-radius: 30upx;
		position: relative;
		display: flex;
		align-items: center;
		margin-top:20upx;
		margin-left: 40upx;
		border: 1px solid #8F8F94;
		
	}
	.st{
		margin-left: 675upx;
		margin-top: -55upx;
	}
	.ss{
		margin-top: 15upx;
		margin-left: 20upx;
	}
	
	.grids{
		margin-top: 20upx;
		height: 140upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		/* border: #000000 1px solid; */
	}
	
	.grids .uni-grid{
		padding-left: 0upx;
		padding-top: -10upx;
		/* height: 550px; */
		/* margin: -30px 0upx; */
	    /* border: #000000 1px solid; */
		/* margin-top: 20upx; */
		
	}
	.grids .uni-grid image{
		height: 100upx;
		width: 130upx;
		border-radius: 10upx;
		border: 1px solid #D2E0E6;
	}
	
	.grid{
		margin-top: 20upx;
		height: 230upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		/* border: #000000 1px solid; */
	}
	
	.grid .uni-grid{
		padding-left: 0upx;
		padding-top: -10upx;
		/* height: 550px; */
		/* margin: -30px 0upx; */
	    /* border: #000000 1px solid; */
		/* margin-top: 20upx; */
		
	}
	.grid .uni-grid image{
		height: 200upx;
		width: 230upx;
		border-radius: 10upx;
		border: 1px solid #D2E0E6;
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
	.te{
		/* border: #000000 1px solid; */
		height: 320upx;
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
	/* .ldh-img{
		border: 1px solid #000000;
		width: 100%;
		height: 130upx;
		margin-top: 20upx;
	}
	.ldh-img image{
		height: 100upx; width: 120upx;
		padding-right: 50upx;
		border: #000000 1px solid;
	} */
	/* .content {
		margin-top: 50upx;
		text-align: center;
		height: 400upx;
	}

	.title {
		font-size: 36upx;
	} */
</style>

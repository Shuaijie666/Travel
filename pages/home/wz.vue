<template>
	<view class="content">
		<view class="top">
		<image src="../../static/img/01.jpg" style="position: absolute; top: 0upx; left: 0upx; z-index: -5; opacity:1; height: 250upx; width: 100%;"></image>
			<view class="bj">
				<text class="t3">北京</text>
				<!-- <image class="ttt" src="../../static/img/wz.png"></image> -->
			</view>
			<view class="sousuo">
				<view class="ss">
					<image src="../../static/img/ss.png" style="width: 50upx; height: 50upx;"></image>
				</view>
				<input placeholder="搜索当地玩乐/美食/路线"/>
			</view>
			<!-- <view class="ty">
				<image src="../../static/img/ty.png" style="width: 50upx; height: 50upx;"></image>
			</view> -->
			<!-- <view class="t5">32度</view> -->
			<view class="t4">
				<text style="color: white; size: 20upx; font-weight: bold;">1314520</text>
				<text style="color: white; size: 5upx;">人正在旅行 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;></text>
			</view>
		</view>
		<view>
			<view class="grid">
				<uni-grid :options='options'  :show-border="false" column-num='5'></uni-grid>
			</view>
		</view>
		
		<view class="scroll_box"> 
			<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
			  <view class="item_a" >
					<image src="../../static/home/rmwf.png" class="item_book_img" mode="aspectFill"></image>
			  </view>
			  <view class="item_b" >
			  		<image src="../../static/home/lyqn.png" class="item_book_img1" mode="aspectFill"></image>
			  </view>
			  <view class="item_c">
			  		<image src="../../static/home/zj.png" class="item_book_img2" mode="aspectFill"></image>
			  </view>
			  <view class="item_d">
			 		<image src="../../static/home/dw.png" class="item_book_img3" mode="aspectFill"></image>
			  </view>
			  <view class="item_e">
			 		<image src="../../static/home/gy.png" class="item_book_img4" mode="aspectFill"></image>
			  </view>
			  <view class="item_f"></view>
			</scroll-view>
		  </view>
		  
		  <view style="">
		  	<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange"></wuc-tab>
		  	<swiper :current="TabCur" duration="300" @change="swiperChange" class="aa">
		  	  <swiper-item v-for="(item,index) in tabList" :key="index">
		  			<view>
		  			<view v-show="TabCur === 0">
						
						<wans></wans>
		  			</view>
		  			<view v-show="TabCur === 1">
		  				<znl></znl>
		  			</view>
		  			<view v-show="TabCur === 2">
		  				<jp></jp>
		  			</view>
		  		</view>
		  	  </swiper-item>
		  	</swiper>
		  </view>
		
	</view>
</template>

<script>
	import WucTab from '@/components/wuc-tab/wuc-tab.vue';
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import wans from "../index/dingwei/wans.vue"
	import znl from "../index/dingwei/znl.vue"
	import jp from "../index/dingwei/jp.vue"
	export default {
		components: {uniGrid,WucTab,wans,znl,jp},
		data() {
			return {
				options:[
				{image:'../../static/img/home/gl.png',text:'攻略'},
				{image:'../../static/img/home/djd.png',text:'景点玩乐'},
				{image:'../../static/img/home/jphcp.png',text:'订酒店'},
				{image:'../../static/img/home/qlx.png',text:'游记'},
				{image:'../../static/img/home/yj.png',text:'行程线路'},
				],
				TabCur: 0,
				tabList: [
					{ name: '怎么玩' }, { name: '住哪里' },
					{ name: '吃什么' }
					
					]

				
			};
		},
		mounted() {
			
		},
		methods:{
		/* 	 scroll: function(e) {
            console.log(e)
            this.old.scrollTop = e.detail.scrollTop
        }, */
		
		tabChange(index) {
		    this.TabCur = index;
		},
		swiperChange(e) {
		    let { current } = e.target;
		    this.TabCur = current;
		}
			
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
	.aa{
		height:2500upx;
		/* border: 1px solid #000000; */
	}
	
	.top{
		/* border: 1px solid #000000 ; */
		height: 250upx;
	}
	.ty{
		display: inline-block;
		padding-left: 20upx;
		padding-top: ;
		
	}
	.ttt{
		width: 35upx;
		height: 35upx;
		padding-left: 10upx;
	}
	.bj{
		width: 17%;
		margin-top: 65upx;
		margin-left: 20upx;
		display: inline-block;
		/* border: 1px solid #000000; */
	}
	.t3{
		color: white;
		size: 10upx;
		font-weight: bold;
	}
	.t4{
		margin-top: -10upx;
		margin-left: 250upx;
		
		
	}
	/* .t5{
		display: inline-block;
		color: white; size: 5upx;
		margin-top: -20upx;
		border: #000000 1px solid;
	} */
	.sousuo{
		width: 80%;
		height: 60upx;
		background-color:#FFF5EE;
		border-radius: 30upx;
		position: relative;
		display: flex;
		align-items: center;
		top: -60upx;
		/* margin-top:-50upx; */
		margin-left: 120upx;
		border: 1px solid #8F8F94;
	}
	.ss{
		margin-top: 15upx;
		margin-left: 20upx;
	}
	
	.scroll_box{width: 95%;height: 130rpx;overflow: hidden;padding: 20rpx;background: #fff;white-space: nowrap;}
	.item_a,.item_b,.item_c,.item_d,.item_e,.item_f{width: 180rpx;height: auto;margin-right: 10rpx;display: inline-block;}
	.item_book_img{width: 70px;height: 60px;border-radius: 10px;}
	.item_book_img1{width: 95px;height: 60px;border-radius: 10px;}
	.item_book_img2{width: 100px;height: 60px;border-radius: 10px;margin-left: 25px;}
	.item_book_img3{width: 100px;height: 60px;border-radius: 10px;margin-left: 55px;}
	.item_book_img4{width: 100px;height: 60px;border-radius: 10px;margin-left: 80px;}

	
	
</style>

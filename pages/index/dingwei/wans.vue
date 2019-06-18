<template>
		<view class="content">
			
				<view class="grid">
					<uni-grid class="uni-grid" :options='options'  :show-border="false" column-num='3' @click='fn'></uni-grid>
				</view>
			
			<view class="titles">
				北京攻略
			</view>
			<view class="grid">
				<uni-grid class="uni-grid" :options='option'  :show-border="false" column-num='3'></uni-grid>
			</view>
			
			<view>
				<view class="title">
					猜你喜欢
				</view>
				<view class="grids">
					<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='2'></uni-grid>
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
				{image:'../../static/img/home/lbj.jpg',text:'故宫全攻略'},
				{image:'../../static/img/home/gg.jpg',text:'观万里长城'},
				{image:'../../static/img/home/cc.jpg',text:'网红拍照地'},
				{image:'../../static/img/home/wh.jpg',text:'老北京胡同'},
				{image:'../../static/img/home/ci.jpg',text:'老北京名吃'},
				{image:'../../static/img/home/sd.jpg',text:'北京必打卡'},
				],
				option:[
				{image:'../../static/img/home/lbj.jpg',text:'北京周边去哪'},
				{image:'../../static/img/home/gg.jpg',text:'假装在国外'},
				{image:'../../static/img/home/cc.jpg',text:'网红拍照地'},
				{image:'../../static/img/home/lbj.jpg',text:'北京周边去哪'},
				{image:'../../static/img/home/gg.jpg',text:'假装在国外'},
				{image:'../../static/img/home/cc.jpg',text:'网红拍照地'}
				],
				//猜你喜欢列表
				
					oppo:[
					{image:'../../static/home/goods/t1.jpg',text:'蛇口价值工厂/免费/涂鸦/废弃style'},
					{image:'../../static/home/goods/t2.jpg',text:'旅游不在乎终点 而是在意途中的人和事'},
					{image:'../../static/home/goods/t3.jpg',text:'伯纳乌球场-马德里'},
					{image:'../../static/home/goods/t4.jpg',text:'伯纳乌球场-马德里'},
					{image:'../../static/home/goods/t5.jpg',text:'停下奔波的脚步，体会自然'},
					{image:'../../static/home/goods/t6.jpg',text:'游船下午茶 杭州西溪悦榕庄'},
					// {image:'../../static/home/goods/t7.jpg',text:'宁夏周边去哪玩'},
					// {image:'../../static/home/goods/t8.jpg',text:'雷阿尔城 柏莱多'},
					// {image:'../../static/home/goods/t9.jpg',text:'红砖美术馆  北京'},
					// {image:'../../static/home/goods/t10.jpg',text:'旅游不在乎终点'},
					]
				
				
			};
		},
		mounted() {
			
		},
		methods:{
			fn(e){
				 console.log(e)
                if(e.index==0){
                 uni.navigateTo({
					url: 'register'
				});
                };
				if(e.index==1){
                 uni.navigateTo({
					url: 'login'
				});
                };
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
		.title {
			font-size: 40upx;
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
	
	
	
	
	
	
	.titles {
			font-size: 50upx;
			text-align: center;
			margin-top: 15upx;
		}
		
		.p1{
			margin-top: 30upx;
			border: #000000 1px solid;
			width: 350upx;
			height: 470upx;
			float: left;
			/* margin-left: 30upx; */
			
		}
		.p1 image{
			border-radius: 10upx;
		}
		
		.p2{
			border: #000000 1px solid;
			width: 350upx;
			height: 470upx;
			float: right;
			margin-top: 30upx;
		}
		.p2 image{
			border-radius: 10upx;
		}
		
		
		
		
		
		/* 猜你喜欢 */
	
</style>

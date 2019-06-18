<template>
	<view class="content">
		<view class="gg" >
			
			<image src="../../static/img/t22.jpg" style="height: 180upx; width: 100%;"></image>
		</view>
		<view>
			<view class="title">
				猜你喜欢
			</view>
			<!-- <view class="grids">
				<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='2'></uni-grid>
			</view> -->
			<view class="product-list">
				<view class="product" v-for="product in productList" :key="product.goods_id">
					<image mode="widthFix" :src="product.img"></image>
					<view class="name">{{ product.name }}</view>
				</view>
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
				//猜你喜欢列表
			/* 	oppo:[
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
				] */
				productList: [
					{
						goods_id: 0,
						img: '../../static/home/goods/t1.jpg',
						name: '蛇口价值工厂/免费/涂鸦/废弃style',
					},
					{
						goods_id: 1,
						img: '../../static/home/goods/t2.jpg',
						name: '旅游不在乎终点 而是在意途中的人和事',
					},
					{
						goods_id: 2,
						img: '../../static/home/goods/t3.jpg',
						name: '伯纳乌球场-马德里',
					},
					{
						goods_id: 3,
						img: '../../static/home/goods/t4.jpg',
						name: '伯纳乌球场-马德里',
					},
					{
						goods_id: 4,
						img: '../../static/home/goods/t5.jpg',
						name: '停下奔波的脚步，体会自然',
					},
					{
						goods_id: 5,
						img: '../../static/home/goods/t6.jpg',
						name: '游船下午茶 杭州西溪悦榕庄',
					},
					{
						goods_id: 6,
						img: '../../static/home/goods/t7.jpg',
						name: '宁夏周边去哪玩',
					},
					{
						goods_id: 7,
						img: '../../static/home/goods/t8.jpg',
						name: '雷阿尔城 柏莱多',
					},
					{
						goods_id: 8,
						img: '../../static/home/goods/t9.jpg',
						name: '红砖美术馆  北京',
					},
					{
						goods_id: 9,
						img: '../../static/home/goods/t10.jpg',
						name: '旅游不在乎终点',
					}
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
	.gg{
		margin-top: 20upx;
	}
	
	.title {
		font-size: 40upx;
		text-align: center;
		margin-top: 15upx;
	}
	
	image {
		height: 300upx;
		width: 100%;
		border-radius: 20upx 20upx 0 0;
	}
	.product {
		width: 48%;
		border-radius: 20upx;
		background-color: #fff;
		margin: 0 0 15upx 0;
		box-shadow: 0upx 5upx 25upx rgba(0, 0, 0, 0.1);
		
		}
		.product-list {
			/* border: #000000 1px solid; */
			width: 92%;
			/* height: 00upx; */
			padding: 0 4% 3vw 4%;
			display: flex;
			justify-content: space-between;
			flex-wrap: wrap;
			margin-top: 20upx;
			}
	.name {
		width: 92%;
		padding: 10upx 4%;
		display: -webkit-box;

		text-align: justify;
		overflow: hidden;
		font-size: 30upx;
	}
	
	
	.grids{
		margin-top: 20upx;
		height: 1900upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		/* border: #000000 1px solid; */
	}
	
	.grids .uni-grid{
		padding-left: 0upx;
		padding-top: -5upx;
		/* height: 550px; */
		/* margin: -30px 0upx; */
	    /* border: #000000 1px solid; */
		/* margin-top: 20upx; */
		
	}
	
	
	.grids .uni-grid image{
		height: 550upx;
		width: 350upx;
		border-radius: 10upx;
		/* border: 1px solid #000000; */
	}
	.grids .uni-grid text{
		font-size: 30upx;
		margin-top: 10upx;
		font-weight: bold;
	}
	
</style>

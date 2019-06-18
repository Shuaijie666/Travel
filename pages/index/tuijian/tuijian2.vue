<template>
	<view class="content">
		<!-- <view>
			 <view class="ldh-img">
			<image src="../../../static/img/tuijian/jpd.jpg"></image>
			<image src="../../../static/img/tuijian/qbj.jpg"></image>
			<image src="../../../static/img/tuijian/sewy.jpg"></image>
		</view> -->
		<view class="grids">
			<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='3'></uni-grid>
		</view>
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
				{image:'../../static/img/tuijian/jpd.jpg'},
				{image:'../../static/img/tuijian/qbj.jpg'},
				{image:'../../static/img/tuijian/sewy.jpg'}
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
	/* .ldh-img{
		border: 1px solid #000000;
		width: 100%;
		height: 130upx;
		margin-top: 20upx;
	} */
	.ldh-img image{
		height: 300upx; width: 240upx;
		padding-left: 10upx;
		border-radius: 10upx;
	}
	.grids{
		height: 300upx;
		width: 100%;
		border-radius: 10upx;
		margin-left: 0upx;
		margin-top: 30upx;
		/* box-shadow: 0 5upx 20upx 0upx rgba(0, 0, 150, .2); */
		/* border: #000000 1px solid; */
	}
	
	.grids .uni-grid{
		padding-left: 0upx;
		padding-top: -5upx;
		height: 400upx;
		/* height: 150px; */
		/* margin: -30px 0upx; */
	    /* border: #000000 1px solid; */
		/* margin-top: 20upx; */
	}
	.grids .uni-grid image{
		height: 400upx;
		width: 240upx;
		border-radius: 10upx;
		/* border: #000000 1px solid; */
	}
</style>

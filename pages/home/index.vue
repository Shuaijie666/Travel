<template>
	<view class="content">
		<!-- 图片 -->
		<view>
		   <swiper class="carousel" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="duration" indicator-color="#FFF">
				<swiper-item>
					<image src="../../static/img/l3.jpg" class="sw-img"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/img/g1.jpeg" class="sw-img"></image>
				</swiper-item>
				<swiper-item>
					<image src="../../static/img/l4.jpg" class="sw-img"></image>
				</swiper-item>
			</swiper>
		</view>
		<!-- 搜索框 -->
		<view class="sousuo">
			<view class="ss">
				<image src="../../static/img/ss.png" style="width: 50upx; height: 50upx;"></image>
			</view>
			<input placeholder="我们去哪里呀" placeholder-style="color:#c0c0c0;"/>
		</view>
		<view class="st">
			<image src="../../static/img/xixi.png" style="width: 50upx; height: 50upx;"></image>
		</view>
		
		<view class="grid">
			<uni-grid :options='options'  :show-border="false" column-num='5'></uni-grid>
		</view>
		<view style="">
			<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange"></wuc-tab>
			<swiper :current="TabCur" duration="300" @change="swiperChange" class="aa">
			  <swiper-item v-for="(item,index) in tabList" :key="index">
					<view>
					<view v-show="TabCur === 0">
						<ly></ly>
					</view>
					<view v-show="TabCur === 1">
						<tj></tj>
					</view>
					<view v-show="TabCur === 2">
						<sp></sp>
					</view>
					<view v-show="TabCur === 3">
						<hd></hd>
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
	import tj from "../index/tj.vue"
	import ly from "../index/ly.vue"
	import sp from "../index/sp.vue"
	import hd from "../index/hd.vue"
	export default {
		components: {uniGrid,WucTab,tj,ly,sp,hd},
		data() {
			return {
				options:[
				{image:'../../static/img/home/gl.png',text:'攻略'},
				{image:'../../static/img/home/djd.png',text:'订酒店'},
				{image:'../../static/img/home/jphcp.png',text:'机票车票'},
				{image:'../../static/img/home/qlx.png',text:'去旅行'},
				{image:'../../static/img/home/yj.png',text:'游记'},
				],
				TabCur: 0,
				tabList: [
					{ name: '正在旅行' }, { name: '推荐' },
					 { name: '国内' }, { name: '海岛旅游' }
					]
				
			};
		},
		mounted() {
			
		},
		methods:{
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
		height:2700upx;
		/* border: 1px solid #000000; */
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
	.grid{
		margin-top: 20upx;
		padding-left: 10upx;
		
	}
</style>

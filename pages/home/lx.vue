<template>
	<view class="content">
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
				<view class="sousuo">
					<view class="ss">
						<image src="../../static/img/ss.png" style="width: 50upx; height: 50upx;"></image>
					</view>
					<input placeholder="我们去哪里呀" class="in"/>
				</view>
		</view>
		
		<view>
			<view class="grid">
				<uni-grid :options='options'  :show-border="false" column-num='5'></uni-grid>
			</view>
		</view>
	 <view class="ldh-img">
			<image src="../../static/img/t11.jpg"></image>
			<image src="../../static/img/t12.jpg"></image>
			<image src="../../static/img/t13.jpg"></image>
		</view> 
		<view>
			<view class="z-text">
				推荐目的地
			</view>
			<view>
				<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange"></wuc-tab>
				<swiper :current="TabCur" duration="300" @change="swiperChange" class="aa">
				  <swiper-item v-for="(item,index) in tabList" :key="index">
						<view>
						<view v-show="TabCur === 0">
							<tuijian1></tuijian1>
						</view>
						<view v-show="TabCur === 1">
							<tuijian2></tuijian2>
						</view>
						<view v-show="TabCur === 2">
							<tuijian3></tuijian3>
						</view>
						<view v-show="TabCur === 3">
							<tuijian4></tuijian4>
						</view>
					</view>
				  </swiper-item>
				</swiper>
			</view>
		</view>
		<view>
			
		</view>
		<view class="te">
			<view  class="te1">精彩周边游</view>
			<view class="te2">健康之旅|一年四季泡温泉竟然都有好处？
			！涨知识！</view>
			<view class="te3">还以为泡温泉只是冬天的专利？那你就out了！泡温泉很多人觉得肯定冬季最好了,
			其实泡温泉一年四季都可以而且应有尽有........</view>
			<view class="grids">
				<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='3'></uni-grid>
			</view>
			
		</view>
		<view class="te">
			<view  class="te1">北京攻略</view>
			<view class="te2">北京西单购物商场评测|看看西单哪里购最便宜？
			！去购物！</view>
			<view class="te3">这是北京的一个地标,以天安门为中心与之对称的还有“东单”,二者均位于长安街北侧！如今都得繁华的商业街,
			潮流界...........</view>
			<view class="grids">
				<uni-grid class="uni-grid" :options='oppo'  :show-border="false" column-num='3'></uni-grid>
			</view>
			
		</view>
		
		<view class="tes">
			<view class="te1">好店好货</view>
			<view class="te2">女神归来--------张敏 横店见面会</view>
			<view class="te3">明星见面会邀你共同参与</view>
			<view class="tu">
				<image src="../../static/img/lx/ns.jpg"></image>
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
		
		
		<view class="loading-text">我是有底线的.....</view>
		
		
		
		
		
		
		
		
		
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import WucTab from '@/components/wuc-tab/wuc-tab.vue';
	import tuijian1 from "../index/tuijian/tuijian1.vue"
	import tuijian2 from "../index/tuijian/tuijian2.vue"
	import tuijian3 from "../index/tuijian/tuijian3.vue"
	import tuijian4 from "../index/tuijian/tuijian4.vue"

	export default {
		components: {uniGrid,WucTab,tuijian1,tuijian2,tuijian3,tuijian4},
		data() {
			return {
				options:[
				{image:'../../static/img/home/gl.png',text:'攻略'},
				{image:'../../static/img/home/djd.png',text:'景点玩乐'},
				{image:'../../static/img/home/jphcp.png',text:'订酒店'},
				{image:'../../static/img/home/qlx.png',text:'游记'},
				{image:'../../static/img/home/djd.png',text:'景点玩乐'},
				{image:'../../static/img/home/jphcp.png',text:'订酒店'},
				{image:'../../static/img/home/qlx.png',text:'游记'},
				{image:'../../static/img/home/yj.png',text:'行程线路'},
				{image:'../../static/img/home/gl.png',text:'攻略'},
				{image:'../../static/img/home/yj.png',text:'行程线路'},
				],
				oppo:[
				{image:'../../static/home/goods/t1.jpg',text:'蛇口价值工厂'},
				{image:'../../static/home/goods/t2.jpg',text:'旅游不在乎终点 '},
				{image:'../../static/home/goods/t3.jpg',text:'伯纳乌球场'},
				],
				TabCur: 0,
				tabList: [{ name: '你关注的' }, { name: '节假日拼假' },
				{ name: '夏日避暑' }, { name: '特价好地' }],
				
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
	.aa{
		/* border: #000000 1px solid; */
		height: 300upx;
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
        /* position: absolute; top: 0upx; left: 0upx;opacity:0.8; height: 60%; width: 80%;	 */	
		width: 80%;
		height: 60upx;
		background-color: white;
		border-radius: 30upx;
		position: absolute; 
		/* display: flex; */
		align-items: center;
		top:50upx;
		left: 60upx;
		/* border: 1px solid #8F8F94; */
		opacity: 0.6;
		display: inline-block;
		
	}
	.ss{
		margin-top: 10upx;
		margin-left: 20upx;
	}
	.in{
		position: absolute; 
		top: 5upx;
		left: 80upx;
	}
	.ldh-img{
		/* border: 1px solid #000000; */
		width: 100%;
		height: 130upx;
		margin-top: 20upx;
	}
	.ldh-img image{
		height: 120upx; width: 240upx;
		padding-left: 10upx;
	}
	.z-text{
		font-size: 40upx;
		font-weight: bold;
		margin-left: 10upx;
	}
	.te{
		/* border: #000000 1px solid; */
		height: 580upx;
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
		height: 1300upx;
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
		height: 500upx;
		width: 240upx;
		border-radius: 10upx;
		/* border: 1px solid #000000; */
	}
	.grids .uni-grid text{
		font-size: 30upx;
		margin-top: 10upx;
		font-weight: bold;
	}
	.tu image{
		height: 280upx;
		width: 100%;
		border-radius: 10upx;
		/* border: #000000 1px solid; */
	}

	/* .content {
		margin-top: 50upx;
		text-align: center;
		height: 3000upx;
		border: 1px solid #000000;
	} */

	/* .title {
		font-size: 36upx;
	} */
</style>

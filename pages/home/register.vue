<template>
	<view class="content">
		<image src="../../static/img/login/timgs.gif" style="position: absolute; top: 0upx; left: 0upx; z-index: -5; opacity:0.8; height: 100%; width: 100%;"></image>
		<view class="is-33vh has-mgt-10">
			<view class="tu">
				<image src="../../static/img/common/heide.jpg" mode="aspectFit" class="logoimg"></image>
			</view>
		</view>
		<view class="registercontent">
			<view class="has-mglr-10 ">
				<view>
					<input type="number" v-model="telno"  placeholder="请输入手机号" />
				</view>
				<view>
					<input type="number"  v-model="xinxi" placeholder="短信验证码" />
					<view class="codeimg" @tap="getsmscode">{{smsbtn.text}}</view>
				</view>

				<view>
				<input :type="flag" placeholder="请输入密码" v-model="password">
				<uni-icon type="eye" size="20" @click='fn'></uni-icon>
				</view>
				<button @click="register">注 册</button>
				
			</view>
		</view>
		<view class="yy">
			<span>
				<text @click="lo" style="color:#F7F7F7;">已有账号立即登录</text>
			</span>
		</view>
		
	</view>
</template>

<script>
	import uniIcon from "@dcloudio/uni-ui/lib/uni-icon/uni-icon.vue"
	export default {
		components: {uniIcon},
		data() {
			return {
				smsbtn: {
					text: '获取验证码',
					status: false,
					codeTime: 60
				},
				timerId: null,
				telno:'',
				password:'',
				xinxi:'',
				flag:'password'
			};
		},
		methods: {
			fn(){
				if(this.flag=='password'){
					this.flag='text'
				}else{
					this.flag='password'
				}
			},
			lo(){
				uni.navigateTo({
					url:'login'
				});
			},
			getsmscode: function() {
				if (this.smsbtn.status == true ) {
					console.log('message：', "别着急！短信已经发送了~");
					return false;
				}
				this.smsbtn.status = true; // 这段代码其实应该加在你request请求 短信发送成功后 
				this.timerId = setInterval(() => {
						var codeTime = this.smsbtn.codeTime;
						codeTime--;
						this.smsbtn.codeTime = codeTime;
						this.smsbtn.text = codeTime + "S";
						if (codeTime < 1) {
							clearInterval(this.timerId);
							this.smsbtn.text = "重新获取";
							this.smsbtn.codeTime = 60;
							this.smsbtn.status = false;
						}
					},
					1000);
				return false;
			},
			register() {
				if(!(/^1(3|4|5|6|7|8|9)\d{9}$/.test(this.telno))){ 
					uni.showToast({title: '请填写正确手机号码',icon:"none"});
					return false; 
				} 
				if (this.xinxi.length <= 0) {
					uni.showToast({
						icon: 'none',
						title: '请输入短信验证码',
						duration: 1000
					});
					return;
				}
				if (this.password.length <= 0) {
					uni.showToast({
						icon: 'none',
						title: '请输入密码',
						duration: 1000
					});
					return;
				}
				else{
					/* switchTab */
					uni.navigateTo({
						url:'login'
					});
					uni.showToast({
						title: '注册成功',
						duration: 2000
					});
				}
				
				

		}
	}
	}
</script>

<style>
	@import url("../../static/css/login.css");
	/* page {
		background-color: #f4f4f4;
		font-size: 35upx;
	}
	.tu{
		text-align: center;
	}

	.registercontent {
		width: 85%;
		margin: 0 auto;
	}

	.logoimg {
		width: 200rpx;
		height: 200rpx;
		border-radius: 50%;
	} */

	/* .is-input1 {
		height: 88rpx;
		width: 100%;
		line-height: 88rpx;
		padding: 12rpx;
		color: #353535;
		font-size: 32rpx;
		box-sizing: border-box;
		appearance: none;
		border: 2rpx solid #e5e5e5;
		box-shadow: none;
		border-radius: 44rpx;
		outline: 0;
		display: block;
		padding-left: 30rpx;
		margin: 0;
		font-family: inherit;
		background: #fff;
		resize: none;

		background: white;
		width: 86%;
		height: 100upx;
		padding-left: 30upx;
		margin: 30upx 5%;
		border-radius: 44upx;
	} */
	/* input{
		background: white;
		width: 86%;
		height: 100upx;
		padding-left: 30upx;
		margin: 30upx 5%;
		border-radius: 44upx;
	}

	.iconfont {
		position: absolute;
		font-size: 40rpx;
		right: 12%;
		z-index: 999;
		width: 105rpx;
		text-align: center;
		color: #353535;
		margin-top: -11%;
		background: #fff;
		border-top-right-radius: 44rpx;
		border-bottom-right-radius: 44rpx;
		height: 80rpx;
		line-height: 80rpx;
	}

	.codeimg {
		position: absolute;
		font-size: 28rpx;
		right: 12%;
		z-index: 999;
		width: 200rpx;
		text-align: center;
		color: #353535;
		margin-top: -15%;
		background: #fff;
		border-top-right-radius: 44rpx;
		border-bottom-right-radius: 44rpx;
		height: 80rpx;
		line-height: 80rpx;
	}


	button {
		width: 90%;
		margin: 50upx 5%;
		border-radius: 44rpx;
		background: #f35;
	}
	.yy{
		margin-left: 90upx;
		margin-top: 50upx;
	}
	.eye{
		margin-left: 500upx;
		margin-top: -100upx;
	} */
</style>

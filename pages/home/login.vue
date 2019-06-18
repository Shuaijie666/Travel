<template>
	<view class="content">
		<image src="../../static/img/login/timgs.gif" style="position: absolute; top: 0upx; left: 0upx; z-index: -5; opacity:0.8; height: 100%; width:100%;"></image>
		<view>
			<view class="tu">
				<image src="../../static/img/common/heide.jpg"  class="logoimg"></image>
			</view>
			<input type="text" placeholder="请输入用户名" v-model="username"/>
			<view>
			<input :type="flag" placeholder="请输入密码" v-model="password">
			<uni-icon type="eye" size="20" @click='fn'></uni-icon>
			</view>
			<button  @click="login">登录</button>
			<view class="text">
			<span class="t1">忘记密码？</span>
			<span @click="register" class="t2">用户注册</span>
			</view>
			<!-- <button  @click="register">注册</button> -->
		</view>
		
		
	</view>
</template>

<script>
	import uniIcon from "@dcloudio/uni-ui/lib/uni-icon/uni-icon.vue"
	export default {	
		components: {uniIcon},
		data() {
			return {
				username:'admin',
				password:'123456',
				flag:'password'	
			};
		},
		mounted() {
			
		},
		methods:{
			register(){
				uni.navigateTo({
					url: 'register'
				});
			},
			fn(){
				if(this.flag=='password'){
					this.flag='text'
				}else{
					this.flag='password'
				}
			},
			
			/* 与后台交互 */
		login(){
			if (this.username.length <= 0) {
					uni.showToast({
						icon: 'none',
						title: '请输入用户名'
					});
					return;
				}
				if (this.password.length <= 0) {
					uni.showToast({
						icon: 'none',
						title: '请输入密码'
					});
					return;
				}
				else{
					/* switchTab */
					uni.switchTab({
						url:'index'
					});
					uni.showToast({
						title: '登录成功',
						duration: 2000
					});
				}
			
				/* uni.request({
					url: this.url+"baseUser/login", //仅为示例，并非真实接口地址。
					data: {
						username: this.username,
						password: this.password
					},
					header: {
						'custom-header': 'hello' //自定义请求头信息
					},
					success: (res) => {
						if(res.data){
							uni.setStorage({
								key: 'baseUser',
								data: res.data
							});
							uni.switchTab({
								url:'index'
							});
							uni.showToast({
								title: '登录成功',
								duration: 2000
							});
							
						}else{
							uni.showToast({
								title: '登录失败',
								duration: 2000
							});
						}
						
					}
				}); */
			}
			/* onNavigationBarButtonTap(){  
				uni.navigateTo({
					url: 'register'
				});		  
			} */
			
		}
	}
</script>

<style>
	@import url("../../static/css/login.css");
	
</style>

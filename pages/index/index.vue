<template>
	<view>
		<web-view :webview-styles="webviewStyles" :src="webViewSrc"></web-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

				webviewStyles: {
					progress: {
						color: '#FF3333'
					}
				},
				// webViewSrc: 'https://dev-xingmou.mvtlabs.com/muyu',
				webViewSrc: 'http://192.168.0.106:1024/muyu'
				// http://192.168.0.106:1024/muyu
			}
		},
		onLoad() {
			setTimeout(() => {
				uni.setNavigationBarTitle({
					title: '3d木鱼'
				})
			}, 2000)
		},
		methods: {
			setBool() {
				this.isTest = !this.isTest
			}
		}
	}
</script>

<style scoped>
	.test {
		width: 200upx;
		height: 200upx;
		background-color: aqua;
		color: #8f8f94;
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>

<template>
	<view class="contact">
		<image class="img" src="../../static/picture/us.jpg" ></image>
		<view class="info">
			<view @click="call">
				联系电话：1234567890（点击拨打）
			</view>
			<view>
				地址：四川省成都市马尼拉县稻香村
			</view>	
		</view>
		<map class="map" longitude="104.065850" latitude="30.657361"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			call(){
				uni.makePhoneCall({
					phoneNumber: '1234567890' 
				});
			}
		}
	}
</script>

<style lang="scss">
	.contact{
		.img{
			width: 750rpx;
			height: 320rpx;
		}
		.info{
			padding: 10rpx 20rpx;
			font-size: 30rpx;
			view{
				line-height: 80rpx;
				border-bottom: 1px solid #eee;
			}
		}
		.map{
			width: 750rpx;
			height: 750rpx;
		}
	}
</style>

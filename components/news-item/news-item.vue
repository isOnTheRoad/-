<template>
	<view>
		
		<view class="news_item" 
		@click="navigator()"
		v-for="item in information"
		 :key="information.id">
			<image :src="item.img_url"></image>
			<view class="right">
				<view class="tit">
					{{item.title}}
				</view>
				<view class="info">
					<text>发表时间:{{item.add_time}}</text>
					<text>浏览次数:{{item.click}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:['information'],
		methods:{
			navigator(){
				this.$emit('itemClick')
			}
		}
	}
	
	
	
</script>

<style lang="scss">
	.news_item{
		display: flex;
		padding: 10rpx 20rpx;
		border-bottom: 1px solid #eee;
		image{
			min-width: 200rpx;
			max-width: 200rpx;
			height: 150rpx;
		}
		.right{
			margin-left: 15rpx;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			.tit{
				font-size: 30rpx;
				}
			.info{
				font-size: 24rpx;	
				text:nth-child(2){
					margin-left:30rpx;
				}
				}
		}
		
	}
</style>
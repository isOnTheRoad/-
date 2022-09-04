<template>
	<view class="pics">
		<scroll-view class="left" scroll-y>
			<view 
			@click="leftClick(index)"
			:class="active===index?'active':''"
			 v-for="(item,index) in message" 
			 :key="item.id">
			{{item.title}}
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				"message":[
				    {"title":"家居生活","id":14},
				    {"title":"摄影设计","id":15},
				    {"title":"明星美女","id":16},
				    {"title":"空间设计","id":17},
				    {"title":"户型装饰","id":18},
				    {"title":"广告摄影","id":19},
				    {"title":"摄影学习","id":20},
				    {"title":"摄影器材","id":21},
				    {"title":"明星写真","id":22},
				    {"title":"清纯甜美","id":23},
				    {"title":"古典美女","id":24}
				  ],
				  active:0
			}
		},
		methods: {
			leftClick(index){
				this.active=index
			}
		}
	}
</script>

<style lang="scss">
page{
	height: 100%;
}
	.pics{
		height:100%;
		.left{
			width: 200rpx;
			height: 100%;
			border-right: 1px solid #eee;
			
			
		}
		view{
			height: 60px;
			line-height: 60px;
			color:#333;
			text-align: center;
			font-size:30rpx;	
			border-top: 1px solid #eee;
			}
		.active{
			background: #b50e03;
			color: #fff;
		}
	}

</style>

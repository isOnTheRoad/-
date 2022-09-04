<template>
	<view class="home">
		<swiper indicator-dots circular>
			<swiper-item v-for="item in message" :key="item.id">
				<image :src="item.img"></image>
			</swiper-item>	
		</swiper>
	<!-- 导航区域 -->
	<view class="nav">
		<view class="nav_item" v-for="(item,index) in navs" :key="index" @click="navItemClick(item.path)">
				<view :class="item.icon"></view>
				<text>{{item.title}}</text>
		</view>
	</view>
	<!-- 推荐商品区 -->
		<view class="hot_goods">
			<view class="title">推荐商品</view>
				<goods-list @goodsItemClick="goGoodsDetail"
				
				 :phone="phone"></goods-list>
			</view>
		</view>
</template>

<script>
	import goodsList from '../../components/goods-list/goods-list.vue'
	export default {
		data() {
			return {
				"message":[
				    {
				    "id":1,
				    "url":"http://www.itcast.cn/subject/phoneweb/index.html",
				    "img":"http://m.itheima.com/images/slidead/mobile/20191213180241750x410.jpg"
				    },        
				    {
				    "id":2,
				    "url":"http://www.itcast.cn/subject/phoneweb/index.html",
				    "img":"http://m.itheima.com/images/slidead/mobile/20191210154717750-410.jpg"
				    },
				    {
				    "id":3,
				    "url":"http://www.itcast.cn/subject/phoneweb/index.html",
				    "img":"http://m.itheima.com/images/slidead/mobile/20190327135101750x410-%E4%BC%A0%E6%99%BA%E9%BB%91%E9%A9%AC%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%B9%BB%E7%81%AF.jpg"
				     }
				  ],
				"phone":[
					{
						"id":1,
						 "adr":"../../static/phone/111.jpg",
						 "title":"小米（XIAOMI）12 64G双4G版",
						 "price":"2199",
						 "market_price":2499,
					},
					{
						"id":2,
						 "adr":"../../static/phone/222.jpg",
						 "title":"华为（HUAWEI）8 16G4G版",
						 "price":"1999",
						 "market_price":2499,
					},
					{
						"id":3,
						 "adr":"../../static/phone/333.jpg",
						 "title":"华为（HUAWEI）ONE 128G电信版",
						 "price":"3299",
						 "market_price":3499,
					},
					{
						"id":4,
						 "adr":"../../static/phone/444.jpg",
						 "title":"AppleXR 64G版",
						 "price":"4999",
						 "market_price":5299,
					},
					{
						"id":5,
						 "adr":"../../static/phone/555.png",
						 "title":"魅族 Mx4 16G联通4G版",
						 "price":"1999",
						 "market_price":2199,
					},
					{
						"id":6,
						 "adr":"../../static/phone/666.jpg",
						 "title":"中兴 理想01 16G移动4G版",
						 "price":"2199",
						 "market_price":2999,
					}
				],
				navs: [
									{
										icon: 'iconfont icon-ziyuan',
										title: '易购超市',
										path: '/pages/goods/goods'
									},
									{
										icon: 'iconfont icon-guanyuwomen',
										title: '联系我们',
										path: '/pages/contact/contact'
									},
									{
										icon: 'iconfont icon-tupian',
										title: '社区图片',
										path: '/pages/pics/pics'
									},
									{
										icon: 'iconfont icon-shipin',
										title: '相关视频',
										path: '/pages/videos/videos'
									}
								]
			}
		},
		components:{
			"goods-list":goodsList
		},
		//导航点击处理函数
		methods:{
			navItemClick(url){
				uni.navigateTo({
					url
				})
			},
			//跳转到商品详情
			goGoodsDetail(id){
				uni.navigateTo({
					url:'/pages/goods-detail/goods-detail?id='+id
				})
			}
		}
	}
</script>

<style lang="scss">
	.home{
		swiper{
			width: 750rpx;
			height: 380rpx;
			image{
				height: 100%;
				width: 100%;
			}
		}
	}
	.nav{
		display: flex;
		.nav_item{
			width: 25%;
			text-align: center;
			text{
				font-size: 30rpx;
			}
			view{
				width: 120rpx;
				height: 120rpx;
				background-color: #b50e03;
				border-radius: 60rpx;
				margin: 10px auto;
				line-height:120rpx;
				color: #fff;
				font-size: 50rpx;
			}
		}
	}
		
	.hot_goods{
		background:#eee;
		overflow: hidden;
		margin-top: 10px;
		.title{
			height: 50px;
			line-height: 50px;
			color: #b50e03;
			text-align: center;
			letter-spacing: 20px;
			background: #fff;
			margin: 7rpx 0;
		}
		
	}
	
</style>

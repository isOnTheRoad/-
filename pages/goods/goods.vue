<template>
	<view class="goods_list">
		<goods-list :phone="phone"></goods-list>
		
	</view>
</template>

<script>
	import goodsList from '../../components/goods-list/goods-list.vue'
	export default {
		data() {
			return {
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
				
			}
		},
			
		components:{
			"goods-list":goodsList
		},
		methods: {
			
		},
			
	}
</script>

<style lang="scss">
.goods_list{
	background: #eee;
}
</style>

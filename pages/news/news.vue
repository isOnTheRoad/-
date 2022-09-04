<template>
	<view class="news">
		<news-item :information="information" @itemClick="goDetail"></news-item>
		
	</view>
</template>

<script>
	import newsItem from '../../components/news-item/news-item.vue'
	export default {
		components:{"newsItem":newsItem},
		data() {
			return {
				 "information":[
				      {"id":13,
				       "title":"1季度多家房企利润跌幅超50% 去库存促销战打响",
				       "add_time":"2015-04-16",
				       "zhaiyao":"房企一季度销售业绩已经陆续公布，克而瑞研究中心统计",
				       "click":1,
				       "img_url":"../../static/picture/che1.jpg"
				      },
					  {"id":14,
					   "title":"1季度多家房企利润跌幅超50% 去库存促销战打响",
					   "add_time":"2015-04-16",
					   "zhaiyao":"房企一季度销售业绩已经陆续公布，克而瑞研究中心统计",
					   "click":2,
					   "img_url":"../../static/picture/che2.jpg"
					  },
					  {"id":15,
					   "title":"1季度多家房企利润跌幅超50% 去库存促销战打响",
					   "add_time":"2015-04-16",
					   "zhaiyao":"房企一季度销售业绩已经陆续公布，克而瑞研究中心统计",
					   "click":2,
					   "img_url":"../../static/picture/che3.jpg"
					  },
					  {"id":16,
					   "title":"1季度多家房企利润跌幅超50% 去库存促销战打响",
					   "add_time":"2015-04-16",
					   "zhaiyao":"房企一季度销售业绩已经陆续公布，克而瑞研究中心统计",
					   "click":2,
					   "img_url":"../../static/picture/che4.jpg"
					  },
					  {"id":17,
					   "title":"1季度多家房企利润跌幅超50% 去库存促销战打响",
					   "add_time":"2015-04-16",
					   "zhaiyao":"房企一季度销售业绩已经陆续公布，克而瑞研究中心统计",
					   "click":2,
					   "img_url":"../../static/picture/che5.jpg"
					  },
				    ],
			}
		},
		methods: {
			goDetail(){
				uni.navigateTo({
					url:'/pages/news-detail/news-detail'
				})
			}
			
		}
	
	}
</script>

<style lang="scss">
	.news{
		
	}
</style>

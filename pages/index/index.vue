<template>
	<view>    <Search></Search>
		<Tickets></Tickets>
		<Classify></Classify>
		<Content id='boxFixed' :class="{'is_fixed':isfixed}"></Content>
		<view style='height: 1500upx;'>
		</view>
	</view>
</template>
<script>
	import Search from './components/search.vue';
	import Tickets from './components/tickets.vue';
	import Classify from './components/classify.vue';
	import Content from './components/content.vue';
	export default {
		components: {
			Search,
			Tickets,
			Classify,
			Content
		},
		data() {
			return {
				scrollTopVal: null,
				isfixed: false,
				fixedScroll: null
			}
		},
		onLoad() {
			const query = wx.createSelectorQuery();
			query.select('#boxFixed')
			.boundingClientRect();
			query.exec(res => {
				console.log(res);
				this.fixedScroll = res[0].top
			})
		},
		onPageScroll(e) {
			this.scrollTopVal = e.scrollTop;
			this.scrollTopVal >= (this.fixedScroll-20)? this.isfixed = true : this.isfixed = false ;
		},
		methods: {}
	}
</script>
<style scoped>
	.is_fixed {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 99;
		transform: translateZ(0);
	}
</style>

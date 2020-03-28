<template>
	<view class="search-container">
		<!-- 搜索 -->

			<view class="search-icon">
				<image src="../../../static/tab/saoma.svg" mode="widthFix"></image>
			</view>
			<view class="search">
				<image src="../../../static/tab/sousuo.svg" mode="widthFix" class="search-img"></image>
				<input type="text" v-model="searchValue" placeholder='请输入文字' disabled/>
			</view>
			<view class="search-icon">
				<image src="../../../static/tab/xiaoxi.svg" mode="widthFix"></image>
			</view>
	
	</view>
</template>
<script>
	export default {
		name: 'search',
		data() {
			return {
			}
		}
	}
</script>
<style scoped>
	.search-icon image{
		width: 50upx;
		height: 50upx;
	}
	.search-icon{
		width: 50upx;
		height: 50upx;
		padding: 0 15upx;
	}
	.search-img{
		width: 40upx;
		height: 40upx;
		margin-left: 20upx;
	}
		
	.search{
		height: 70upx;
		line-height: 70upx;
		width: 100%;
		display: flex;
		background-color: #fff7d4;
		align-items: center;
		border-top-left-radius: 50upx;
		border-bottom-left-radius: 50upx;
		border-bottom-right-radius: 50upx;
	}
	.search input{
		height: 70upx;
		line-height: 70upx;
		width: 100%;
		font-size: 30upx;
		color:#66666;
	}
	.search-container{
		display: flex;
		justify-content: space-between;
		height: 70upx;
		align-items: center;
		background: linear-gradient(to top,#ffe566 10%,#ffd300 100%);
		padding: 30upx 0;
	}
</style>

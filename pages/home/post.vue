<template>
	<view class="content">
		<view>
			<image style="width:600upx; height: 100upx;" :mode="item.mode" src="../../static/imgs/yizhan/yzlogo.png"></image>
		</view>
		<view>
			<!--驿站代收 -->
			<view class="yizhan">
				<view class="yizhan1"><image style="width:130upx; height: 130upx;" :mode="item.mode" src="../../static/imgs/yizhan/yizhan1.png"></image></view>
				<view class="yizhan1"><p class="p1">驿站代收</p><p>上班，上课，旅游，不怕没人收包裹</p></view>
			</view>
			<!-- 便捷寄件 -->
			<view class="yizhan">
				<view class="yizhan1"><image style="width:130upx; height: 130upx;" :mode="item.mode" src="../../static/imgs/yizhan/yizhan2.png"></image></view>
				<view class="yizhan1"><p class="p1">便捷寄件</p><p>寄件不用等，家门口即可寄件</p></view>
			</view>
			<!-- 安全保管 -->
			<view class="yizhan">
				<view class="yizhan1"><image style="width:130upx; height: 130upx;" :mode="item.mode" src="../../static/imgs/yizhan/yizhan3.png"></image></view>
				<view class="yizhan1"><p class="p1">安全保管</p><p>包裹丢失必赔偿，安全有保障</p></view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		mounted() {
			
		},
		methods:{
			
		}
	}
</script>

<style>
	@import url("../../static/css/yizhan.css");
</style>

<template>
	<view class="content">
		<view>
			<view slot="left" class="scan">
				<!-- 扫一扫 -->
				<view style="float: left;"><uni-icon type="scan" size="24"></uni-icon></view>
				<!-- 文本输入框 -->
				<view style="float: left; margin-left: 115upx;"><input class="uni-input" focus placeholder="一键查全网包裹" /></view>
				<!-- 消息图标 -->
				<view style="float: left; margin-left: 125upx;"><image style="width:60upx; height: 60upx;" :mode="item.mode" src="../../static/imgs/tidings.png"></image></view>
			</view>
			<!-- 滑动轮播图 -->
			<view>
				<uni-swiper-dot :info="info" :current="current" field="content" :mode="mode">
					<swiper class="swiper-box" @change="change" autoplay="autoplay">
						<swiper-item v-for="(item ,index) in info" :key="index">
							<view class="swiper-item">
								<image :src="item.content" mode=""></image>
							</view>
						</swiper-item>
					</swiper>
				</uni-swiper-dot>
			</view>
			<!-- 九宫格 -->
			<uni-grid :options="[
				{image:'../../static/imgs/gg1.png',text:'寄快递'},
				{image:'../../static/imgs/gg2.png',text:'领裹酱'},
				{image:'../../static/imgs/gg3.png',text:'我的亲友'},
				{image:'../../static/imgs/gg4.png',text:'精灵书屋'},
				{image:'../../static/imgs/gg5.png',text:'蓝犀牛搬家'},
				{image:'../../static/imgs/gg6.png',text:'手机回收'},
				{image:'../../static/imgs/gg7.png',text:'包裹大作战'},
				{image:'../../static/imgs/gg8.png',text:'玩具租赁'},
				{image:'../../static/imgs/gg9.png',text:'数码租赁'},
				{image:'../../static/imgs/gg10.png',text:'女装租赁'}]"
			 show-border="false" column-num="5">
			</uni-grid>
		</view>

	</view>
</template>

<script>
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniSwiperDot from "@/components/uni-swiper-dot/uni-swiper-dot.vue"
	export default {
		components: {
			uniIcon,
			uniGrid,
			uniSwiperDot
		},
		data() {
			return {
				info: [{
					content: '../../static/imgs/lb2.jpg'
				}, {
					content: '../../static/imgs/lb3.png'
				}],
				current: 0,
				mode: 'long',
			}
		},
		mounted() {

		},
		methods: {
			change(e) {
				this.current = e.detail.current;
			}
		}
	}
</script>

<style>
	@import url("../../static/css/shouye.css");
</style>

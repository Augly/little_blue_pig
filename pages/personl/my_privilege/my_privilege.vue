<template>
	<view class="my_privilege">
		<view class="my_privilege_scroll">
			<scroll-view class="my_privilege_scroll_wrap" scroll-x="true">
				<view :class="activeClass(index)" v-for="(item,index) in 10" @click.stop="checkThis(index)">
					<view class="scroll_title">猪一戒会员</view>
					<view class="scroll_discount">9.5折</view>
					<view class="scroll_price">￥18.00</view>
				</view>
			</scroll-view>
		</view>
		<view class="my_privilege_nav">
			<view class="my_privilege_nav_title">会员特权</view>
			<view class="my_privilege_nav_list">
				<view class="my_privilege_nav_item">
					<view class="my_privilege_nav_item_icon">
						<image src="../../../static/49.png"></image>
					</view>
					<view>赠送蓝珠</view>
					<view>100:1抵用租金</view>
				</view>
				<view class="my_privilege_nav_item">
					<view class="my_privilege_nav_item_icon">
						<image src="../../../static/49.png"></image>
					</view>
					<view>设备租金</view>
					<view>7.5折</view>
				</view>
				<view class="my_privilege_nav_item">
					<view class="my_privilege_nav_item_icon">
						<image src="../../../static/49.png"></image>
					</view>
					<view>免押额度增加</view>
					<view>1000.00</view>
				</view>
				<view class="my_privilege_nav_item">
					<view class="my_privilege_nav_item_icon">
						<image src="../../../static/49.png"></image>
					</view>
					<view>会员有效期</view>
					<view>30天</view>
				</view>
			</view>
		</view>
		<view class="my_privilege_ul">
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/47.png"></image>
				<view class="my_privilege_li_title">会员有效期</view>
				<view class="my_privilege_li_badge">30</view>
			</view>
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/13.png"></image>
				<view class="my_privilege_li_title">优先发货</view>
				<view class="my_privilege_li_badge">顺丰速达</view>
			</view>
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/14.png"></image>
				<view class="my_privilege_li_title">抵扣租金</view>
				<view class="my_privilege_li_badge">蓝珠抵扣</view>
			</view>
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/4.png"></image>
				<view class="my_privilege_li_title">包邮次数</view>
				<view class="my_privilege_li_badge">3次/月</view>
			</view>
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/50.png"></image>
				<view class="my_privilege_li_title">蓝珠</view>
				<view class="my_privilege_li_badge">10000</view>
			</view>
			<view class="my_privilege_li">
				<image class="my_privilege_li_icon" src="../../../static/22.png"></image>
				<view class="my_privilege_li_title">设备租金</view>
				<view class="my_privilege_li_badge">7.5折</view>
			</view>
		</view>
		<view class="my_privilege_btn_top"></view>
		<view class="my_privilege_btn" @click.stop="makeVip()">￥188.00去开通会员</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				currentIndex: 0
			};
		},
		methods: {
			activeClass(index) {
				return index == this.currentIndex ? 'my_privilege_scroll_item active' : 'my_privilege_scroll_item'
			},
			checkThis(index) {
				this.currentIndex = index
			},
			makeVip() {
				uni.showToast({
					title: '开通会员',
					mask: false,
					icon: 'none',
					duration: 1500
				});
			}
		}
	}
</script>

<style>
	.my_privilege {
		background: #F7F7F7;
		padding-top: 55.55upx;
	}

	.my_privilege_scroll {
		white-space: nowrap;
		width: 100%;
	}

	.my_privilege_scroll_wrap {
		white-space: nowrap;
		width: 100%;
	}

	.my_privilege_scroll_item {
		box-sizing: border-box;
		display: inline-block;
		white-space: nowrap;
		width: 258.33upx;
		height: 201.38upx;
		margin-right: 13.88upx;
		background: #FFFFFF;
		text-align: center;
		color: #000000;
		border-radius: 4.16upx;
		border: 1.38upx solid #A9744F;
	}
	.my_privilege_scroll_item.active {
		background-image: url('~@/static/33.png');
		background-repeat: no-repeat;
		background-size: cover;
		color: #FFFFFF;
	}
	.scroll_title {
		font-size: 22.91upx;
		padding-top: 34.72upx;
	}
	.scroll_discount {
		font-size: 45.83upx;
		padding-top: 13.88upx
	}
	.scroll_price {
		font-size: 20.83upx;
		padding-top: 13.88upx
	}
	
	.my_privilege_scroll_item:first-child {
		margin-left: 20.83upx
	}
	.my_privilege_scroll_item image{
		width: 100%;
		height: 100%;
	}
	.my_privilege_nav {
		margin-top: 55.55upx;
		width: 100%;
		height: auto;
		background: #FFFFFF;
	}
	.my_privilege_nav_title {
		font-size: 33.33upx;
		padding: 33.33upx 0 47.22upx 27.77upx;
	}
	.my_privilege_nav_list {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		padding-bottom: 65.27upx;
	}
	.my_privilege_nav_item {
		display: flex;
		flex-direction: column;
		width: 24.4%;
		align-items: center;
	}
	.my_privilege_nav_item view:nth-child(2) {
		font-size: 22.22upx;
		padding-top: 26.38upx;
		color: #666666;
	}
	.my_privilege_nav_item view:nth-child(3) {
		font-size: 19.44upx;
		padding-top: 19.44upx;
		color: #999999;
	}
	.my_privilege_nav_item_icon {
		width: 77.08upx;
		height: 77.08upx;
	}
	.my_privilege_nav_item_icon image {
		width: 100%;
		height: 100%;
	}
	.my_privilege_ul {
		width: 100%;
		height: auto;
		background: #FFFFFF;
		margin-top: 20.83upx;
	}
	.my_privilege_li {
		display: flex;
		flex-direction: row;
		height: 94.44upx;
		line-height: 94.44upx;
		border-bottom: 1.38upx solid #e5e5e5;
	}
	.my_privilege_li_icon {
		width: 34.72upx;
		height: 34.72upx;
		margin-left: 20.83upx;
		margin-top: 34.72upx;
		margin-right: 20.83upx;
	}
	.my_privilege_li_title {
		flex: 1;
	}
	.my_privilege_li_badge {
		font-size: 22.22upx;
		color: #181818;
		text-align: center;
		width: 156.94upx;
	}
	.my_privilege_btn_top {
		background: #f0f4f7;
		height: 131.94upx;
	}
	.my_privilege_btn {
		width: 100%;
		background-image: linear-gradient(163deg, #dcaf67 2%, #e8b67b 100%), linear-gradient(#f76d4a, #f76d4a);
		color: #FFFFFF;
		position: fixed;
		left: 0;
		bottom: 0;
		height: 90.27upx;
		line-height: 90.27upx;
		text-align: center;
	}
	
</style>

<template>
<view class="ikea">
	<div class="logo">
		<img src="/static/LOGO.png" alt />
	</div>
	<div class="jion">
		<b>欢迎加入</b>
		<b>宜家会员俱乐部</b>
	</div>
	<div class="return">
		<div class="return-btn"><a @click="backMemberCenter">返回会员中心</a><uni-icons type="contact" size="30"></uni-icons></div>
	</div>
</view>
</template>

<script>
import uniIcons from "../../../components/yangxiaochuang-icons/yangxiaochuang-icons"
export default {
components: {uniIcons},
data() {
	return {};
},
onLoad() {},
methods: {}
};
</script>

<style>
.logo {
	width: 100%;
	height: 270rpx;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #0077c8;
	}

img {
	width: 213rpx;
	height: 90rpx;
	}

.jion {
	width: 100%;
	height: 220rpx;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	}
	
b {
	display: block;
	font-size: 60rpx;
	color: #0077c8;
	}
.return{
	width: 100%;
	display: flex;
	align-items: flex-end;
	justify-content: center;
	position: absolute;
	bottom: 60rpx;
	color:#8f8f8f;
}


</style>

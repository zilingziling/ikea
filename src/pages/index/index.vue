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
		<div class="return-btn"><div style="display:in-lineblock:font-size:16px;" @click="backMemberCenter">{{text}}<uni-icons type="arrowright" color='#8f8f8f' size="16"></uni-icons></div></div>
	</div>
</view>
</template>

<script>
import uniIcons from "../components/uni-icons/uni-icons"
export default {
	components: {uniIcons},
data() {
	return {
		text:'返回会员中心'
	};
},
onLoad() {},
methods: {
	backMemberCenter(){
		console.log('点击返回会员中心')
	}
}
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

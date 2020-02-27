<template>
	<div class="verify">
		<div class="content">
			<div class="logo">
				<img src="../../static/LOGO.png" alt="">
			</div>
			<div class="prompt">
				<div class="prompt-info">
					<b>定制你的专属会员优惠</b>
				</div>
			</div>
			<div class="data">
				<view>
					<view class="uni-common-mt">
						<view class="uni-form-item uni-column">
							<view class="title">手机号</view>
							<input class="uni-input topInput" placeholder-style="color:rgba(100,100,100,1);font-size:30rpx;font-weight:400" placeholder="请填写您的手机号" focus placeholder="自动获得焦点" />
						</view>
						<view class="uni-form-item uni-column">
							<view class="title">验证码</view>
							<input class="uni-input botInput" placeholder-style="color:rgba(100,100,100,1);font-size:30rpx;font-weight:400"  placeholder="请输入您的验证码" />
						</view>
					</view>
				</view>
				<div class="data-verification">
					<a v-if="showVerifyErr"> <i>warningIcon</i> 验证码输入有误，请重新输入</a>
					<span v-if="getCodeBtn" :style="{background:(ifGetCode? '#0077c8':'#dcdcdc'),color:(ifGetCode?'#fff':'#787878')}" >获取验证码</span>
					<span v-if="!getCodeBtn" :style="{background:(ifGetCode? '#dcdcdc':'#dcdcdc'),color:(ifGetCode?'#787878':'#787878')}" >{{verifyTime}}s后重新获取</span>
				</div>
			</div>
			<div class="agree">
				<label>
				<checkbox v-model="outboundSmsFlag" icon-size='.24rem' shape="square"/>
					我愿意接受来自宜家俱乐部的短信
				</label>
			</div>
			<div class="progress">
				<span class="progress-percentage">0%</span>
				<span class="progress-border"><b></b></span>
			</div>
			<div class="confirm">
				<div class="confirm-btn"><button type="primary" :disabled='!ifGetCode' >下一步</button></div>
			</div>
		</div>
	</div>
</template>

<script>

	export default {

		components: {},
		data() {
			return {
				tel:'',
				verifyCode:'',
				outboundSmsFlag:true,
				ifGetCode:false,
				showVerifyErr:false,
				showPhoneErr:'',
				verifyTime:60,
				getCodeBtn:true,//显示获取验证码按钮
				infoData:{},
				requestId:'',
			};
		},
		computed: {},
		watch: {},
		methods: {

		},
		created() {

		},
		mounted() {},
	}
</script>
<style lang='less' scoped>
	@import "../../styles/common.less";
	.verify{
		.content{
			.logo{
				width: 100%;
				height: 1.75rem;
				display: flex;
				justify-content: center;
				align-items: flex-end;
				img{
					width: 2.13rem;
					height: .9rem;
				}
			}
			.prompt{
				padding-top: .4rem;
				&-info{
					height: 1.2rem;
					// margin-top: .6rem;
					display: flex;
					flex-direction: column;
					align-items: center;
					justify-content: center;
					font-size:40rpx;
					font-family:NotoIKEASimplifiedChinese;
					font-weight:bold;
					color:rgba(0,119,200,1);
				}
			}
			.data{
				padding: 0 .9rem;
				height: 5.5rem;
				display: flex;
				flex-direction: column;
				justify-content: center;
				.title{
					font-size:30rpx;
					font-family:NotoIKEASimplifiedChinese;
					font-weight:bold;
					color:rgba(50,50,50,1);
					margin-bottom: 20rpx;
				}
				.uni-input{
					width:570rpx;
					height:70rpx;
					background:rgba(255,255,255,1);
					border:1rpx solid rgba(100,100,100,1);
				}
				.topInput{
					margin-bottom: 51rpx;
				}
				.botInput{
					margin-bottom: 35rpx;
				}

				&-info{
					height: 1.65rem;
					&-title{
						color: rgb(50, 50, 50);
						font-size: .28rem;
						display: block;
						margin-bottom: .2rem;
					}
				}
				&-verification{
					height: .54rem;
					// display: flex;
					// justify-content: space-between;
					span{
						width: 2.55rem;
						height: .54rem;
						border-radius: .3rem;
						text-align: center;
						line-height: .54rem;
						color: #fff;
						// background: #0077c8;
						float: right;
					}
					a{
						display: flex;
						color: red;
						align-items: center;
						width: 2.5rem;
						float: left;
						font-size: .24rem;
					}
				}
			}
			.agree{
				height: 1rem;
				padding: 0 .9rem;
				font-size: .24rem;
				display: flex;
				margin-top: 1rem;
					align-items: center;
				// align-items: flex-end;
			}
			.progress{
				height: 1rem;
				display: flex;
				flex-direction: column;
				padding: 0 .9rem;
				&-percentage{
					text-align: center;
					height: .5rem;
					color: #0077c8;
					font-weight: bold;
				}
				&-border{
					width: 100%;
					height: .08rem;
					border-radius: .04rem;
					background: #dcdcdc;
					display: flex;
					b{
						height: 100%;
						width: 0%;
						background: #0077c8;
						border-radius:.04rem;
					}
				}
				// padding: 0 .9rem;
				// font-size: .24rem;
				// display: flex;
			}
			.confirm{
				width: 100%;
				height: 1rem;
				margin-bottom: 1rem;
				display: flex;
				justify-content: center;
				align-items: center;
				flex-direction: column;
				&-btn{
					text-align: center;
					width: 5.65rem;
					line-height: .8rem;
					height: .8rem;
					border-radius: .4rem;
					color:#939393;
				}
			}
			.msg{
				padding: 0.2rem .7rem;
				font-size: .28rem;
				color: #b0b0b0;
				a{
					color: #0077c8;
				}
			}
		}
	}
</style>

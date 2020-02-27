<template>
    <div class="verify">
        <div class="content">
            <div class="logo">
                <img src="/static/LOGO.jpg" alt="">
            </div>
            <div class="prompt">
                <div class="prompt-info">
                    <b>请完成身份信息验证</b>
                    <b>顺利找回电子会员卡</b>
                </div>
                <div class="prompt-text">
                    <p>您的资料仅用于身份验证并受到<div class="ys"  @click="openPrivacy">隐私政策</div>保护 </p>
                </div>
            </div>
            <div class="data">
                <div class="data-info">
                        选择
                </div>
            </div> 
            <div class="confirm">
                
                <div class="confirm-btn">按钮</div>
                <div class="confirm-contact">
                    <a @click="openPrompt">联系客服</a>
                    <a @click="backMemberCenter">返回会员中心</a>
                </div>
            </div>
        <!-- 验证弹窗提示
            <van-dialog
                v-model="showDialog"
                title="联系客服"
                confirmButtonText="返回继续验证"
            >
                <div class="msg">需帮助,请拨打客服电话 <a href="tel:400-800-2345">400-800-2345</a> 或直接联系<a href="https://amos.alicdn.com/getcid.aw?spm=a1z10.1-b-s.1997427721.2.69a31d884kaTwt&v=3&groupid=0&s=1&charset=utf-8&uid=ikea%E5%AE%9C%E5%AE%B6%E5%AE%B6%E5%B1%85%E5%AE%98%E6%96%B9%E6%97%97%E8%88%B0%E5%BA%97&site=cntaobao&fromid=cntaobaoikea%D2%CB%BC%D2%BC%D2%BE%D3%B9%D9%B7%BD%C6%EC%BD%A2%B5%EA">淘宝客服</a>获得帮助</div>
            </van-dialog>
        <!-- 下拉选项 -->
            <!-- <van-popup
                v-model="showSelect"
                position="bottom"
                :style="{ height: '3rpx' }"
            >
                <van-picker
                    show-toolbar
                    :visible-item-count	= 3
                    :columns="columns"
                    @cancel="showSelect = false"
                    @confirm="onConfirm"
                    safe-area-inset-bottom
                />
            </van-popup> -->
        <!-- 隐私协议 -->
            <!-- <van-popup v-model="showPrivacy" round>
                <privacy/>
            </van-popup> -->
        </div> -->
    </div>
</template>

// <script>
// import moment from 'moment';
// import {memberURL} from '../api/index'
// import privacy from './privacy'
// export default {
    
//     components: {
//         privacy
//     },
//     data() {
//         return {
//             option:'',
//             showDialog:false,
//             showPrivacy:false,
//             showSelect:false,
//             btnColor:'#939393',
//             columns: ['姓名', '生日'],
//             info:{}
//         };
//     },
//     computed: {},
//     watch: {},
//     methods: {
//         openPrompt(){
//             this.showDialog = true
//         },
//         openPrivacy(){
//             this.showPrivacy = true
//         },
//         openpicker(){
//             this.showSelect = true
//         },
//         onConfirm(value) {
//             this.option =value;
//             this.btnColor = '#0077c8';
//             this.showSelect = false;
//         },
//         next(){
//             if(this.option == '姓名'){
//                 // this.info.phone = this.$route.query.phone
//                 this.info.tel = this.$route.query.tel
//                 this.$router.push({ name: 'nameverify', query: this.info})
//             }else if(this.option == '生日'){
//                 // this.info.phone = this.$route.query.phone
//                 this.info.tel = this.$route.query.tel
//                 this.$router.push({ name: 'birthdayverify', query: this.info})
//             }else{
//                 return '';
//             }
//         },
//         backMemberCenter(){
//             window.location.href = memberURL
//         }
//     },
//     created() {
//         this.info = this.$route.query
//         console.log(this.info)
//     },
//     mounted() {},
//     }
// </script>
<style lang='less' scoped>
// @import "../styles/common.less";

.verify{
    // background: #f7f8fa;
    .content{
        .logo{
            width: 100%;
            height: 175rpx;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            img{
                width: 213rpx;
                height: 90rpx;
            }
        }
        .prompt{
            padding: 40rpx 0;
            &-info{
                height: 120rpx;
                font-size: 40rpx;
                color: #0077c8;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
            }
            &-text{
                display: flex;
                justify-content: center;
                text-align: center;
                font-size: 26rpx;
                color: #8f8f8f;
                .ys{
                    color: #0077c8;
                }
                
            }
        }
        .data{
            padding: 20rpx 90rpx;
            height: 500rpx;
            &-info{
                height: 150rpx;
                margin-bottom: 30rpx;
                margin-top: 200rpx;
                &-title{
                    color: rgb(50, 50, 50);
                    font-size: 28rpx;
                    display: block;
                    margin-bottom: 20rpx;
                }
            }
        }
        .confirm{
            width: 100%;
            height: 200rpx;
            padding: 50rpx 0;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            &-btn{
                text-align: center;
                width: 565rpx;
                line-height: 80rpx;
                height: 80rpx;
                border-radius: 40rpx;
                color:#939393;
            }
            &-contact{
                width: 565rpx;
                height: 100rpx;
                display: flex;
                justify-content: space-between;
                align-items: flex-end;
                a{
                    color: #b0b0b0;
                    display: flex;
                    height: 30rpx;
                    line-height: 30rpx;
                }
            }
        }
    }
    .msg{
            padding: 20rpx 70rpx;
            font-size: 28rpx;
            color: #b0b0b0;
            a{
                color: #0077c8;
            }
        }
}
</style>
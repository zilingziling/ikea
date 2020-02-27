<template>
    <div class="member">
        <div class="member-family">
            <div class="member-family-content">
                <img src="../../static/family.png" alt="">
                <div class="member-family-content-welcome">
                    <p>欢迎加入 <span>宜家俱乐部</span> </p>
                    <p>用灵感点亮你的家居梦想</p>
                </div>
            </div>
        </div>
        <img class="member-large" src="../../static/largeFamily.png">
        <img class="member-feature" src="../../static/actDetail.png">
        <div class="member-btn">
            <button type="primary"  class="member-btn-new">新会员注册</button>
            <button type="default"  class="member-btn-old">我是老会员</button>
        </div>
        <div class="member-return">
            <a @click="backMemberCenter">返回会员中心 > </a>
        </div>
    </div>
</template>

<script>
// import {memberURL} from '../api/index'
export default {
components: {},
data() {
return {

};
},
computed: {},
watch: {},
methods: {
backMemberCenter(){
window.location.href = ""
}
},
created() {
// console.log(this.$route)
},
mounted() {}
};

</script>
<style lang='less' scoped>
@import "../../styles/common.less";
.member{
    height: auto;
    // height: 13.4rpx;
    background: #ffffff;
    &-family{
        width: 100vw;
        height: 213rpx;
        display: flex;
        justify-content: center;
        align-items: center;
        padding:58rpx 54rpx;
        box-sizing: border-box;
        &-content{
            width: 100%;
            display: flex;
            justify-content: space-between;
            flex-direction: row;
            align-items: center;
            img{
                width: 148rpx;
                height: 109rpx;
            }
            &-welcome{
                width: 459rpx;
                color:rgba(0, 119, 200, 1);
                font-size: 42rpx;
                display: flex;
                flex-direction: column;

                p{
                    white-space: nowrap;
                    font-family: NotoIKEASimplifiedChinese-Bold;
                    span{
                        font-weight: bold;
                    }
                }
            }
         }
    }
    &-large{
             width: 100%;
            height: 360rpx;
        }
    &-feature{

        width: 746rpx;
        height: 360rpx;
        margin: auto;

        // background: #ccc;
    &-t{
            width: 100%;
            display: flex;
            justify-content: center;
        &-jion{
                display: flex;
                align-items: center;
                padding: 0 15rpx;
                // width: 2.55rpx;
                height: 93rpx;
                // background: red;
            &-l{
                    font-size: 20rpx;
                    img{
                        width: 51rpx;
                        height: 55rpx;
                        color: black;
                    }
                    b{
                        font-size: 50rpx;
                    }
                }
            &-r{
                    display: flex;
                    flex-direction: column;
                    margin-left: 10rpx;
                &-t{
                        font-size: 36rpx;
                    }
                &-b{
                        font-size: 20rpx;
                    }
                }
            }
        }
    &-b{
            margin-top: 20rpx;
            width: 100%;
            display: flex;
            justify-content: center;
        &-jion{
                display: flex;
                align-items: center;
                padding: 0 15rpx;
                height: 93rpx;
            &-l{
                    font-size: 20rpx;
                    img{
                        width: 41rpx;
                        height: 44rpx;
                        color: black;
                    }
                    b{
                        font-size: 50rpx;
                    }
                }
            &-r{
                    display: flex;
                    flex-direction: column;
                    margin-left: 10rpx;
                &-t{
                        font-size: 36rpx;
                    }
                &-b{
                        font-size: 20rpx;
                    }
                }
            }
        }
    }
&-btn{
        /*margin-top: 100rpx;*/
        padding: 0 90rpx;
        height: 200rpx;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        // background: yellow;
        &-new{
            height: 80rpx;
            width: 570rpx;
            border-radius:40rpx;
            background:rgba(0,119,200,1);
            font-size:30rpx;
            font-family:NotoIKEASimplifiedChinese;
            font-weight:bold;
            color:rgba(255,255,255,1);
            line-height: 80rpx;
        }
    &-old{
        height: 80rpx;
        width: 570rpx;
        border-radius:40rpx;
        border:2rpx solid rgba(85,85,85,1);
        font-size:30rpx;
        font-family:NotoIKEASimplifiedChinese;
        font-weight:bold;
        color:rgba(35,35,35,1);
        line-height: 80rpx;
    }
    }
&-return{
            height: 150rpx;
        display: flex;
        justify-content: center;
        align-items: center;
    a{

        font-size:28rpx;
        font-family:NotoIKEASimplifiedChinese;
        font-weight:400;
        color:rgba(85,85,85,1);
    }
}
}
</style>

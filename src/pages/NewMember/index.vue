<template>
    <div class="member">
        <div class="member-family">
            <img src="../../static/family.png" alt="">
            <div class="member-family-welcome">
                <span>欢迎加入 <b>宜家俱乐部</b> </span>
                <span>用灵感点亮你的家居梦想</span>
            </div>
        </div>
        <img class="member-large" src="../../static/largeFamily.png">
        <div class="member-feature">
            <span class="member-feature-t">
                <span class="member-feature-t-jion">
                    <a class="member-feature-t-jion-l">￥<b>10</b> </a>
                    <a class="member-feature-t-jion-r">
                        <b class="member-feature-t-jion-r-t">入会有礼</b>
                        <a class="member-feature-t-jion-r-b">满减优惠券</a>
                    </a>
                </span>
                <span class="member-feature-t-jion">
                    <a class="member-feature-t-jion-l"> <img src="../../static/product.jpg" alt=""> </a>
                    <a class="member-feature-t-jion-r">
                        <b class="member-feature-t-jion-r-t">特惠产品</b>
                        <a class="member-feature-t-jion-r-b">每月会员折扣</a>
                    </a>
                </span>
                <span class="member-feature-t-jion">
                    <a class="member-feature-t-jion-l"><img src="../../static/birthday.png" alt=""></a>
                    <a class="member-feature-t-jion-r">
                        <b class="member-feature-t-jion-r-t">生日惊喜</b>
                        <a class="member-feature-t-jion-r-b">￥10优惠券</a>
                    </a>
                </span>
            </span>

            <span class="member-feature-b">
                <span class="member-feature-b-jion">
                    <a class="member-feature-b-jion-l"> <img src="../../static/activity.png" alt=""> </a>
                    <a class="member-feature-b-jion-r">
                        <b class="member-feature-b-jion-r-t">专享活动</b>
                        <a class="member-feature-b-jion-r-b">家居知识讲座</a>
                    </a>
                </span>
                <span class="member-feature-b-jion">
                    <a class="member-feature-b-jion-l"> <img src="../../static/guarantee.png" alt=""> </a>
                    <a class="member-feature-b-jion-r">
                        <b class="member-feature-b-jion-r-t">安心保障</b>
                        <a class="member-feature-b-jion-r-b">退换货时间延长</a>
                    </a>
                </span>
            </span>
            <span class="member-feature-b">

            </span>
        </div>
        <div class="member-btn">
<!--            <van-button type="primary" color='#0077c8' round size="large" to="newverifyphone">新会员注册</van-button>-->
<!--            <van-button type="default"  round size="large" to="phoneverify">我是老会员</van-button>-->
        </div>
        <div class="member-return">
<!--            <a @click="backMemberCenter">返回会员中心<van-icon name="arrow" /></a>-->
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
// backMemberCenter(){
// window.location.href = memberURL
// }
},
created() {
// console.log(this.$route)
},
mounted() {}
}
</script>
<style lang='less' scoped>
@import "../../styles/common.less";
.member{
    height: 100%;
    // height: 13.4rem;
    // background: #ccc;
&-family{
        width: 100%;
        height: 2.15rem;
        display: flex;
        justify-content: center;
        align-items: center;
        img{
            width: 1.5rem;
            height: 1rem;
            margin-left: .3rem;
        }
    &-welcome{
            width: 4.7rem;
            height: 1rem;
            color:#0077c8;
            font-size: .4rem;
            display: flex;
            flex-direction: column;
            margin-left: .4rem;
        }
    }
&-large{
        width: 100%;
        height: 3.6rem;
    }
&-feature{
        width: 100%;
        height: 2.7rem;
        display: flex;
        margin-top: .3rem;
        flex-direction: column;
        justify-content: center;
        // background: #ccc;
    &-t{
            width: 100%;
            display: flex;
            justify-content: center;
        &-jion{
                display: flex;
                align-items: center;
                padding: 0 .15rem;
                // width: 2.55rem;
                height: .93rem;
                // background: red;
            &-l{
                    font-size: .2rem;
                    img{
                        height: .55rem;
                        color: black;
                    }
                    b{
                        font-size: .5rem;
                    }
                }
            &-r{
                    display: flex;
                    flex-direction: column;
                    margin-left: .1rem;
                &-t{
                        font-size: .36rem;
                    }
                &-b{
                        font-size: .2rem;
                    }
                }
            }
        }
    &-b{
            margin-top: .2rem;
            width: 100%;
            display: flex;
            justify-content: center;
        &-jion{
                display: flex;
                align-items: center;
                padding: 0 .15rem;
                height: .93rem;
            &-l{
                    font-size: .2rem;
                    img{
                        height: .55rem;
                        color: black;
                    }
                    b{
                        font-size: .5rem;
                    }
                }
            &-r{
                    display: flex;
                    flex-direction: column;
                    margin-left: .1rem;
                &-t{
                        font-size: .36rem;
                    }
                &-b{
                        font-size: .2rem;
                    }
                }
            }
        }
    }
&-btn{
        margin-top: 1rem;
        padding: 0 .9rem;
        height: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        // background: yellow;
    }
&-return{
        height: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    a{
        display: flex;
        height: .3rem;
        line-height: .3rem;
        color: #b0b0b0;
    }
}
}
</style>

<!--
    /**
     * Description: 加入车商城，告别库存积压
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="inventory">
        <h2 class="my-title"> 加入车商城，告别库存积压</h2>

        <div class="content">
            <shop-intro-l class="user animated" :init="user" :class="[animation?'slideInLeft':'slideOutLeft']"></shop-intro-l>

            <shop-intro-l class="way animated" :init="way" :class="[animation?'slideInLeft':'slideOutLeft']"></shop-intro-l>

            <!-- 高精准销售线索-->
            <shop-intro-r class="precise animated" :init="precise" :class="[animation?'slideInRight':'slideOutRight']"></shop-intro-r>
            <!-- 大型活动-->
            <shop-intro-r class="active animated" :init="active" :class="[animation?'slideInRight':'slideOutRight']"></shop-intro-r>
        </div>
    </div>
</template>

<style scoped lang="less" rel="stylesheet/less">
    @import "../common/css/maxin.less";
    .inventory{
        @bg:#fff;
        background: @bg;
        .skew(@bg);
    }
    .positionAb(@top:auto,@right:auto,@bottom:auto,@left:auto){
        position: absolute;
        top: @top;
        right: @right;
        bottom: @bottom;
        left: @left;
    }
    .content{
        position: relative;
        height: 400px;
        background: url(https://s.kcimg.cn/wap/images/storeroadcast/phone.png) no-repeat 46% top;
        background-size: contain;
        &:after{
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 103px;
            background: rgba(255,255,255,.97);
        }
         .active{
             .positionAb(auto,50px,125px)
         }
         .precise{
            .positionAb(40px,23px)
         }
        .user{
            .positionAb(-35px,auto,auto,53px)
        }
        .way{
            .positionAb(auto,auto,190px,25px)
        }
    }


</style>


<script type="text/babel">
    import myTitle from './title.vue'
    import shopIntroR from './carShopIntroR.vue'
    import shopIntroL from './carShopIntroL.vue'

    export default{
        props:['animation'],
        data: function () {
            return {
                precise:{
                    lean: {width:'40px',transform: 'rotateZ(-26deg)',marginTop: '-24px'},
                    line:{},
                    text:'高精准销售线索 客户在线支付定金',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/precise.png) no-repeat center'}
                },
                active: {
                    lean: {},
                    line:{},
                    text:'定期举办大型活动 团购、秒杀、特定…',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/active.png) no-repeat center'}
                },
                user:{
                    lean: {},
                    line:{},
                    text:'庞大的卡友用户群体 200万潜在购车用户',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/user.png) no-repeat center'}
                },
                way:{
                    lean: {width:'30px',transform: 'rotateZ(36deg)',marginTop:'-24px',marginLeft:'-4px'},
                    line:{},
                    text:'多样促销方式 一口价、抵扣券...',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/way.png) no-repeat center'}
                }
            }
        },
        components: {
            myTitle,
            shopIntroR,
            shopIntroL
        },
        created: function () {
        },
        methods: {}
    }

</script>


 
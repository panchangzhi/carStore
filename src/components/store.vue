<!--
    /**
     * Description: 5步玩转车商城
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="store">
        <h2 class="my-title"> 5步玩转车商城</h2>
        <div class="content">
            <play class="animated" :class="[animation?'zoomIn':'zoomOut']" :init="uploading"></play>
            <play class="animated" :class="[animation?'zoomIn':'zoomOut']" :init="order"></play>
            <play class="animated" :class="[animation?'zoomIn':'zoomOut']" :init="record"></play>
            <play class="animated" :class="[animation?'zoomIn':'zoomOut']" :init="deal"></play>
            <play class="animated" :class="[animation?'zoomIn':'zoomOut']" :init="broadcast"></play>
        </div>
    </div>
</template>

<style scoped lang="less">
    @import "../common/css/maxin.less";

    .store{
        height: 1190px;
        @bg:#fff;
        background: @bg;
        .skew(@bg);
        .content{
            margin-top: -20px;
        }
    }


</style>

<script type="text/babel">
    import myTitle from './title.vue'
    import play from './playingStep.vue'


    export default{
        data: function(){
            return {
                uploading:{
                    title:'上传商品',
                    text:'将商品上传至车商城 立刻获得200万卡友关注',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/uploading.png) no-repeat center'}
                },
                order:{
                    title:'买家下单',
                    text:'待卡友在车商城支付车辆 定金，迅速锁定高精准买 家目标',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/order.png) no-repeat center'}
                },
                record:{
                    title:'跟进记录',
                    text:'联系买家并在订单中记录 跟进情况，分析买家价值 成交量更高',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/record.png) no-repeat center'}
                },
                deal:{
                    title:'订单成交',
                    text:'买家到店验车支付尾款 高效完成交易，卖车轻轻松',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/deal.png) no-repeat center'}
                },
                broadcast:{
                    title:'活动宣传',
                    text:'参加大型促销活动，更快获 得高精准买家，订单扑面来',
                    icon:{background:'url(https://s.kcimg.cn/wap/images/storeroadcast/broadcast.png) no-repeat center'}
                }
            }
        },
        props:['animation'],
        components:{
            myTitle,
            play
        },
        created: function(){

        },
        methods:{

        }
    }

</script>

 
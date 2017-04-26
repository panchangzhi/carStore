<!--
    /**
     * Description: 打开销售的无限可能
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="infinite">
        <!--<my-title value="打开销售的无限可能"></my-title>-->
        <h2 class="title"> 打开销售的无限可能</h2>
        <div class="content">

        </div>
    </div>
</template>

<style scoped lang="less">
    @import "../common/css/maxin.less";

    .infinite{
        height: 1070px;
    @bg:#f6f7fc;
        background: @bg url(https://s.kcimg.cn/wap/images/storeroadcast/sale_bg.jpg) no-repeat center 120px;

    .skew(@bg);
    }
    .title{
        padding: 63px 195px;
        box-sizing: border-box;
        line-height: 40px;
        font-weight: 500;
        font-size: 40px;
    }
</style>

<script type="text/babel">
    import myTitle from './title.vue'

    export default{
        data: function(){
            return {}
        },
        components:{
            myTitle
        },
        created: function(){

        },
        methods:{

        }
    }

</script>


 
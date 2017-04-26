<!--
    /**
     * Description: footer
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="footer">
        Copyright © 2016 卡车之家 All rights reserved
    </div>
</template>

<style scoped lang="less">
    @import "../common/css/maxin.less";

    .footer{
        height: 95px;
        line-height: 95px;
        text-align: center;
        font-size: 24px;
        color: #ccc;
        @bg:#fff;
        background: @bg;
        .skew(@bg);
    }
</style>

<script type="text/babel">
    export default{
        data: function(){
            return {}
        },
        props:[],
        components:{},
        created: function(){

        },
        methods:{

        }
    }

</script>


 
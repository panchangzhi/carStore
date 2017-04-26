<!--
    /**
     * Description: 加入车商城，这些都能卖
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="sale">
        <h2 class="my-title"> 加入车商城，这些都能卖</h2>


        <div class="content ">
            <div>
                <span class="circle animated pulse infinite"  >新车</span>
                <span class="circle animated pulse infinite" >库存车</span>
                <span class="circle animated pulse infinite"  >定制车</span>
                <span class="circle animated pulse infinite"  style="margin:0">新能源车</span>
            </div>

            <div>
                <span class="circle animated pulse infinite" >专用车</span>
                <span class="circle animated pulse infinite" >工程车</span>
                <span class="circle animated pulse infinite" style="margin:0" >进口车</span>
            </div>

        </div>
    </div>
</template>

<style scoped lang="less">
    @import "../common/css/maxin.less";

    .sale{
        height: 490px;
        @bg:#f6f7fc;
        background: @bg;
        .skew(@bg);
    .content{
        &>div{
              margin: 0 auto;

                &:first-child{
                 width: 580px;
                }
    &:last-child{
         width: 426px;
     }
          }
        .circle{
            float: left;
            margin-right: 30px;
            height: 120px;
            width: 120px;
            line-height: 120px;
            text-align: center;
            color: #49b4ff;
            font-size: 24px;
            border-radius: 50%;
            border: 1px solid #49b4ff;
            box-shadow: 0 0 5px 0 #49b4ff;

        }
        }
    }
</style>

<script type="text/babel">
    import myTitle from './title.vue'
    import myCircle from './circle.vue'

    export default{
        data: function(){
            return {}
        },
        props:['animation'],
        components:{
            myTitle,
            myCircle
        },
        created: function(){

        },
        methods:{

        }
    }

</script>


 
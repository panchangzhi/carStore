<template>
    <div class="alert-wrapper" @touchmove.prevent>

        <article id="alert-box">



                <header class="alert-title"><h3>申请成功</h3></header>
                <section class="alert-con">
                    <p>请您保持手机畅通，区域经理会在3天内与您联系！</p>
                    <p>免费入驻电话  400-819-6168</p>
                </section>

            <aside class="alert-confirm" @click="alert">知道了</aside>
        </article>
    </div>
</template>
<script type="text/babel">
    export default {
        props:[],
        create(){

        },
        methods:{
            alert(){
                this.$emit('alert');
            }
        }
    }
</script>
<style>
    /*弹层背景*/
    .alert-wrapper{
        position: fixed;
        width: 100%;
        top:0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(0,0,0,.5);
        z-index: 1;
    }
    /*弹层内容*/
    #alert-box{
        width: 75%;
        background-color: #fff;
        padding-top: 5px;
        text-align: center;
        border-radius: 10px;
        position: absolute;
        top: 0;
        margin-top: 367px;
        bottom: auto;
        left: 12.5%;
        z-index: 2;
    }
    .alert-title{
        width: 100%;
        color: #333;
        font: 28px/110px 'Helvetica Neue';
    }
    .alert-con{
        height: 158px;
        width: 80%;
        margin: 0 auto;
    }
    .alert-con p{
        line-height: 46px;
        font-size: 26px;
        color: #666;
    }
    .alert-confirm{
        height: 96px;
        line-height: 96px;
        font-size: 26px;
         border-top: 1px solid #e9e9e9;
        color: #008af4;
    }
    .warn{
        line-height: 46px;
        font-size: 26px;
        color: #666;
    }
</style>
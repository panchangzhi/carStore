<template>
    <div class="playing-step">
        <span class="step-img" :style="init.icon"></span>
        <dl class="step-intro">
            <dt>{{init.title}}</dt>
            <dd>
                {{init.text}}
            </dd>
        </dl>
    </div>
</template>

<script type="text/babel">
    export default{
        data: function(){
            return {}
        },
        props:['init'],
        created: function(){

        },
        methods:{

        }
    }
</script>

<style scoped>
    dl, dd,body{
        margin: 0;
    }
    .playing-step{
        width: 50%;
        height: 355px;
        float: left;
    }
    .step-img{
        display: block;
        margin: 0 auto;
        width: 140px;
        height: 140px;
        border-radius: 50%;
        background-color: #49b4ff;
    }
    .step-intro{
        text-align: center;
    }
    .step-intro dt{
        font-size: 28px;
        height: 60px;
        line-height: 60px;
        font-weight: 400;
        color: #333;
    }
    .step-intro dd{
        padding: 0 63px 0 43px;
        font-size:22px;
        line-height: 36px;
        box-sizing: border-box;
        color: #768491;
    }
</style>
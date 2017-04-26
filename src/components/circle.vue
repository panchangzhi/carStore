<!--
    /**
     * Description: 
     * author: panchanzhi
     * date: 2017/4/18
     */
-->

<template>
    <span class="circle">
        {{text}}
    </span>
</template>

<style scoped lang="less">
    .circle{
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
</style>

<script type="text/babel">
    export default{
        data: function(){
            return {}
        },
        props:['text'],
        components:{},
        created: function(){

        },
        methods:{

        }
    }

</script>


 
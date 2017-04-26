<!--
    /**
     * Description: title
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div>
        <h1 class="title">{{value}}</h1>
    </div>
</template>

<style scoped>
    .title{
        width: 100vw;
        padding: 63px 0;
        box-sizing: border-box;
        line-height: 40px;
        font-weight: 500;
        font-size: 40px;
        text-align: center;
    }
</style>

<script type="text/babel">
    export default{
        data: function(){
            return {}
        },
        props:['value'],
        created: function(){

        },
        methods:{

        }
    }

</script>


 
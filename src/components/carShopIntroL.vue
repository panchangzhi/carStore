<!--
    /**
     * Description: 加入车商城，告别库存积压
     * author: panchanzhi
     * date: 2017/4/18
     */
-->
<template>
    <div class="car-shop-intro">
        <span class="circle-type" :style="init.icon"></span>
        <span class="line" :style="init.line"></span>
        <span class=" lean-line" :style="init.lean"></span>
        <span class="circle-point"></span>
        <p class="text">{{init.text}}</p>
    </div>
</template>

<script type="text/babel">
    export default {
        props: ['init']
    }
</script>

<style scoped>
    .car-shop-intro {
        position: relative;
        display: flex;
        margin-top: 100px;
        align-items: center;
        /*width: 289px;*/
    }

    .car-shop-intro span {
        display: block;
    }

    .circle-point {
        width: 6px;
        height: 6px;
        margin-left: -3px;
        border-radius: 50%;
        background-color: #49b4ff;
    }

    .lean-line {
        transform: rotateZ(21deg);
        width: 56px;
        margin-top: -22px;
        height: 1px;
        margin-left: -2px;
        background-color: #49b4ff;
    }

    .line {
        margin-top: -43px;
        width: 150px;
        border-bottom: 1px solid #49b4ff;
        font-size: 16px;
        line-height: 24px;
        padding-bottom: 2px;
        text-align: center;
        padding-left: 22px;
        padding-right: 10px;
        box-sizing: border-box;

    }
    .text{
        position: absolute;
        top: -65px;
        left: 57px;
        width: 145px;
        font-size: 16px;
        color: #333;
        display: -webkit-box;
        text-overflow: ellipsis;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
        overflow: hidden;
    }

    .circle-type {
        width: 58px;
        height: 58px;
        border: 1px solid #3f9dfb;
        background-color: #fff;
        border-radius: 50%;
        margin-top: -38px;
    }
</style>
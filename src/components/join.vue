<!--
    /**
     * Description: 免费加入 免费入驻电话
     * author: panchanzhi
     * date: 2017/4/17
     */
-->

<template>
    <div class="join">
        <a class="join-item" href="javascript:;" @click="call">免费入驻电话</a>
        <a class="join-item" href="javascript:;" @click="fetch">免费加入</a>
    </div>
</template>

<style scoped lang="less">
    .join {
        height: 98px;
        line-height: 98px;
        text-align: center;
        border-top: 2px solid #ccc;

    .join-item {
        float: left;
        width: 50%;

    &:nth-of-type(1) {
        font-size: 30px;
        color: #333;

    &:before {
        content: "\e6ed";
        margin-right: 10px;
        font-family: iconfont;
        color: #49b4ff;

    }

    }
    &:nth-of-type(2) {
        font-size: 36px;
        color: #fff;
        background: #49b4ff;
    }

    }
    }
    .title {
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
    import axios from 'axios'

    export default{
        data: function () {
            return {}
        },
        props: [],
        components: {},
        created: function () {
            //获取storage
            let storage = localStorage.getItem('vipLodData');
            storage = storage? JSON.parse(storage):{};
            this.dealerId = storage.dealerid;
        },
        methods: {
            alert(){
                this.$emit('alert');
            },
            fetch(){
                ga('send', 'event','点击免费加入','点击免费加入','');
                axios.get(`https://dealer-mall.360che.com/dealer-join?dealer_id=${this.dealerId}`).then((response)=> {
                    if(response.data.code > 0){
                        this.alert();
                    }
                    else{
                    }
                }).catch(function (error) {
                    console.log(error);
                });
            },
            call(){
                ga('send', 'event','点击免费入驻电话','点击免费入驻电话','');

                this.$nextTick(
                    function(){
                        location.href="tel:4008196168";
                    }
                )
            },

        }
    }

</script>

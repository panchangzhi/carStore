<template>
    <div id="app" class="container" ref='container' @scroll="scroll">
        <banner class="item" :animation="defaultH[0] || currentIndex == 0"></banner>
        <inventory class="item" id="inventory" :animation="defaultH[1] || currentIndex == 1"></inventory>
        <sale class="item" id="sale" :animation="defaultH[2] || currentIndex == 2"></sale>
        <store class="item" id="store" :animation="defaultH[3] || currentIndex == 3"></store>
        <infinite class="item"id="infinite" :animation="defaultH[4] || currentIndex == 4" style="text-align: center"></infinite>
        <my-footer></my-footer>
        <join class='join-wrapper' @alert="alert"></join>
        <alert v-if="show" @alert="alert"></alert>
    </div>
</template>

<script type="text/babel">
    import banner from './components/banner'
    import inventory from './components/inventory'
    import sale from './components/sale.vue'
    import store from './components/store.vue'
    import infinite from './components/infinite.vue'
    import myFooter from './components/footer.vue'
    import join from './components/join.vue'
    import alert from './components/applicationAlert.vue'

    export default {
        name: 'app',
        components: {
            banner,
            inventory,
            sale,
            store,
            infinite,
            myFooter,
            join,
            alert
        },
        data(){
            return {
                show: false,
                animation:[],
                height: window.screen.availHeight,
                listHeight:[],
                scrollY:0,
                defaultH:[],
                dealerId:''

            }
        },
        created(){
            this.$nextTick(function(){
                this.calculateHeight();
                for(let i=0;i < this.listHeight.length;i++){
                    if(this.height> this.listHeight[i]){
                        this.defaultH[i] = true
                    }
                }
                this.defaultH.push(true);
            })
        },
        methods:{

            alert(msg){//弹层
                this.show = !this.show;
                this.msg = msg;
            },
            calculateHeight() {//计算区间
                let itemList = this.$refs.container.querySelectorAll('.item');
                let height = 0;

                this.listHeight.push(height);

                for (let i = 0; i < itemList.length; i++) {
                    let item = itemList[i];
                    height += item.clientHeight;
                    this.listHeight.push(height);
                }
            },
            scroll(){//滚动事件
                this.scrollY = event.target.scrollTop+this.height;
            }
        },
        computed:{
            currentIndex(){//计算移动到的区间
                for (let i = 0; i < this.listHeight.length; i++) {
                    let heightPre = this.listHeight[i];
                    let heightNext = this.listHeight[i + 1];
                    if (!heightNext || (this.scrollY >= heightPre && this.scrollY < heightNext)) {
                        this.defaultH[i] = false;
                        return i;
                    }
                }
                return 0;
            }
        },
        mounted(){

        }
    }
</script>

<style>
    @import "common/css/reset.css";
    @import "common/css/font.less";

    .container{
        height: 100%;
        padding-bottom: 100px;
        overflow-y: auto;
        overflow-x: hidden;
        box-sizing: border-box;
        -webkit-overflow-scrolling: touch;
    }
    .animated{
        animation-duration:0.5s;
    }
    .my-title{
        display: inline-block;
        position: relative;
        left: 50%;
        transform: translateX(-50%);
        padding: 63px 0;
        box-sizing: border-box;
        line-height: 40px;
        font-weight: 500;
        font-size: 40px;
    }
    .join-wrapper{
        position: fixed;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: 50;
        background: #fff;
    }
</style>

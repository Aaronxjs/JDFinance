<template>
    <Panel title="生活服务" :class="$style.panel">
        <section :class="$style.content">
            <ul v-for="(item, index) in items" :key="index">
                <li><img :src="item.url"/></li>
                <li><p>{{item.title}}</p></li>
                <li><p>{{item.text}}</p></li>
            </ul>
        </section>
    </Panel>
</template>
<script>
    import Panel from "../core/panel.vue"
    export default{
        components:{
            Panel
        },
        data(){
            return {
                items:[
                    {
                        url: "//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135",
                        title: "惠加油",
                        text: ""
                    },
                    {
                        url: "//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132",
                        title: "小白信用",
                        text: "全新升级"
                    },
                    {
                        url: "//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135",
                        title: "信用卡还款",
                        text: ""
                    },
                    {
                        url: "//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135",
                        title: "卡转让",
                        text: ""
                    },
                    {
                        url: "//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135",
                        title: "定期还款",
                        text: ""
                    }
                ] 
            }
        }
    };
</script>
<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel($color: #333);
        .content{
            font-size: 26px;
            width: 100%;
            @include list(row);
            align-items: flex-start;
            justify-content: space-between;
            padding-bottom: 20px;
            ul{
                @include list();
                justify-content: center;
                align-items: center;
                flex:1;
                width: 20%;
                li{
                    width: 100%;
                    margin-top: 10px;
                    text-align: center;
                    img{
                        width: 90px;
                        height: 90px;
                    }

                }
                &:nth-child(2){
                    li{
                        &:last-child{
                            color: #ff0000;
                        }
                    }

                }
                p{
                    overflow: hidden;
                    text-overflow: ellipsis;
                    white-space: nowrap;
                }
            }
        }
    }
</style>

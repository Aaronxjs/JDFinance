<template>
    <Panel title="理财精选" :class="$style.panel">
        <section :class="$style.content">
            <dl v-for="(list, index) in lists" :key="index">
                <dt>
                    <span>{{ list.name }}</span>
                    <span>{{ list.base }}</span>
                </dt>
                <dd>
                    <span>{{ list.rate }}</span>
                </dd>
                <dd>
                    <span>{{ list.laber }}</span>
                </dd>
            </dl>
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
                lists:[
                    {
                        name: "定期理财",
                        base: "理财首选",
                        rate: "5.60%",
                        laber: "历史年化回报率"
                    },
                    {
                        name: "小白理财",
                        base: "理财首选",
                        rate: "4.22%",
                        laber: "7日年化收益率"
                    },
                    {
                        name: "月月盈",
                        base: "养老保障",
                        rate: "5%",
                        laber: "7日年化收益率"
                    },
                    {
                        name: "小白基金",
                        base: "天天赚钱",
                        rate: "4.27%",
                        laber: "7日年化收益率"
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
        >h4{
            border-bottom: 1px solid #ccc;
            box-shadow: 0 2px 3px -1px #888888;
        }
        .content{
            font-size: 26px;
            width: 100%;
            @include list(row);
            align-items: flex-start;
            justify-content: center;
            dl{
                width: 50%;
                box-sizing: border-box;
                padding: 20px 20px;
                text-align: center;
                dt{
                    display: -webkit-inline-box;
                    margin-top: 10px;
                    span{
                        &:last-child{
                            font-size: 20px;
                        }
                    }
                }
                dd{
                    margin-top: 10px;
                    &:last-child{
                        font-size: 20px;
                        color: #888888;
                    }  
                    &:nth-child(2){
                        font-size: 28px;
                        color: #ff0000;
                    }
                }
            }
            span{
                display: block;
            }
            dt{
                span:last-child{
                    color: #ff0000;
                    border: 1px solid #ff0000;
                }
            }
        }
    }
</style>

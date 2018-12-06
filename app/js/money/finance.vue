<template>
    <Panel title="理财精选" :class="$style.panel">
        <section :class="$style.content">
            <ul>
                <li>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76" alt=""/>
                </li>
                <li>
                    <h4>月度理财</h4>
                    <p>预期年化收益率4.50%</p>
                </li>
                <li>去赚钱 > </li>
            </ul>
            <ul>
                <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76" alt=""/></li>
                <li>
                    <h4>季度理财</h4>
                    <p>历史年化回报率5.50%</p>
                </li>
                <li>去赚钱 > </li>
            </ul>
            <ul>
                <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76" alt=""/></li>
                <li>
                    <h4>一年理财</h4>
                    <p>历史年化回报率5.80%</p>
                </li>
                <li>去赚钱 > </li>
            </ul>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components:{
        Panel
    }
}
</script>
<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel($color: #333);
        .content{
            @include list();
            ul{
                padding: 20px 0px;
                border-top: 1px solid #aaaaaa;
                @include list(row);
                justify-content: space-between;
                align-items: center;
                li{
                    flex-grow:1;
                    h4{
                        font-size: 24px;
                        margin-bottom: 10px;
                    }
                    p{
                        width: 200px;
                        font-size: 20px;
                        color: #ff0000;
                        overflow:hidden;
                        text-overflow: ellipsis;
                        white-space: nowrap;
                    }
                    &:first-child{
                        img{
                            width: 60px;
                            height: 60px;
                        }
                        text-align: center;
                    }
                    &:nth-child(2){
                        flex-grow:2;
                    }
                    &:last-child{
                        text-align: center;
                        font-size: 22px;
                        color:#EEAD0E;
                    }
                }
            }
        }
    }
</style>

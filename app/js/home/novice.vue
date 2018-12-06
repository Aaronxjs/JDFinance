<template>
    <Panel title="新手特权" :class="$style.panel">
        <section class="clearfloat" :class="$style.novice">
            <ul :class="$style.item">
                <li class="text-center">下载APP<span class="red">送888元礼包</span></li>
                <li class="text-center"><span class="gray">新手专享</span></li>
                <li class="text-center"><img src="//img12.360buyimg.com/jrpmobile/jfs/t10384/155/1759179594/9776/185bd062/59e5f0ebNec4cf494.png?width=100&height=100"/></li>
            </ul>
            <ul :class="$style.item">
                <li>
                    <div :class="$style.float">
                        <ul class="clearfloat">
                            <li ><span class="red">领188元新手</span>...</li>
                            <li><span class="gray">立即开通</span></li>
                        </ul>
                    </div>
                    <div :class="$style.float">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t4639/162/1782623297/60754/98ea03b4/58e60952N7fdb2b85.png?width=200&height=200"/>
                    </div>
                </li>
                <li>
                    <div :class="$style.float">
                        <ul class="clearfloat">
                            <li>打白条<span class="red">享免息</span></li>
                            <li><span class="gray">立即开通享好礼</span></li>
                        </ul>
                    </div>
                    <div :class="$style.float">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t4804/179/657713323/5908/66dce262/58e6095fNd3dc3f39.png?width=100&height=100"/>
                    </div>
                </li>
            </ul>
        </section>
    </Panel>
</template>
<script>
    import Panel from "../core/panel.vue"
    export default{
        components: {
            Panel
        }
    };
</script>
<style lang="scss">
    @import "../../css/common.scss";
</style>
<style lang="scss" module>
    @import "../../css/element.scss";

    .float{
        float:left;
        margin-left: 30px;
    }
    .novice{
        height: 180px;
        @include list(row);
        padding:10px 0px; 
        .item{
            width: 50%;
            height: 100%;
            font-size: 26px;
            box-sizing:border-box;
            &:first-child{
                border-right: 1px solid #ccc;
                li{
                    margin-top: 5px;
                    img{
                        width: 100px;
                        height: 100px;
                    }
                }
            }
            &:nth-child(2){
                @include list(row);
                >li{
                   height: 50%;
                   @include list(row);
                   align-items:center;
                   justify-content: center;
                }
            }
            >li{
                text-align: center;
                width: 100%;
                li{
                    margin-top: 5px;
                }
            }
            div{
                img{
                    width: 60px;
                    height: 60px;
                }
            }
            section{
                margin: 10px 0px;
            }
        }
    }
    .panel{
        @include panel($color: #333);
        >h4{
            border-bottom: 1px solid #ccc;
            box-shadow: 0 2px 3px -1px #888888;
        }
    }
</style>
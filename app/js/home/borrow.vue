<template>
    <Panel title="极速借贷" :class="$style.panel">
        <section :class="$style.content">
            <router-link to="name">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t12721/42/2497849749/26333/ec584be4/5a421756N2416c88f.png?width=750&height=280"/>
            </router-link>
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
<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel($color: #333);
        >h4{
            border-bottom: 1px solid #ccc;
            box-shadow: 0 2px 3px -1px #888888;
        }
        .content{
            @include list();
            align-items: center;
            justify-content: center;
            img{
                width: 100%;
                height: 100%;
            }
        }
    }
</style>

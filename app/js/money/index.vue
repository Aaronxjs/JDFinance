<template>
    <div>
        <Header></Header>
        <Mslider></Mslider>
        <Ada></Ada>
        <Money></Money>
        <Adb></Adb>
        <Finance></Finance>
        <Adc></Adc>
        <Footer :class="$style.cname"></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import Footer from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Mslider from "./mslider.vue"
import Money from "./money.vue"
import Ada from "./ada.vue"
import Adb from "./adb.vue"
import Adc from "./adc.vue"
import Finance from "./finance.vue"
export default {
    components:{
        Header,
        Footer,
        Navbar,
        Mslider,
        Ada,
        Adb,
        Adc,
        Money,
        Finance
    }
}
</script>
<style lang="scss" module>
    @import "../../css/reset.scss";
    .cname{
        li{
            &:first-child{
                display: none;
            }
        }
    }
</style>



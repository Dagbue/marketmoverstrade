<template>
  <div class="alpha">
    <p class="section-header-1">A world of stocks at your fingertips</p>
    <p class="section-header">From technology to healthcare, New York to Hong Kong, Market Movers empowers traders with
      real-time access to stocks from top exchanges worldwide.</p>


    <div class="section-navigation">

      <p @click="changeScreen" class="nav-item">Popular Stocks</p>

      <p @click="changeScreen2" class="nav-item">Forex</p>

      <p @click="changeScreen3" class="nav-item">Crypto</p>

<!--      <p class="nav-item">Durable goods</p>-->
    </div>


    <div v-show="this.screen === 'crypto'" class="section-alpha">
      <nvda-widget/>
      <apple-widget/>
      <google-widget/>
      <meta-widget/>
    </div>

    <div v-show="this.screen === 'forex'" class="section-alpha">
      <euro-widget/>
      <gbp-widget/>
      <jyp-widget/>
      <chf-widget/>
    </div>

    <div v-show="this.screen === 'stocks'" class="section-alpha">
      <btc-widget/>
      <eth-widget/>
      <usdt-widget/>
      <usdc-widget/>
    </div>

  </div>
</template>


<script>
import NvdaWidget from "@/components/BaseComponents/widgets/NvdaWidget.vue";
import AppleWidget from "@/components/BaseComponents/widgets/AppleWidget.vue";
import GoogleWidget from "@/components/BaseComponents/widgets/GoogleWidget.vue";
import MetaWidget from "@/components/BaseComponents/widgets/MetaWidget.vue";
import EuroWidget from "@/components/BaseComponents/widgets/EuroWidget.vue";
import GbpWidget from "@/components/BaseComponents/widgets/GbpWidget.vue";
import JypWidget from "@/components/BaseComponents/widgets/JypWidget.vue";
import ChfWidget from "@/components/BaseComponents/widgets/ChfWidget.vue";
import BtcWidget from "@/components/BaseComponents/widgets/BtcWidget.vue";
import EthWidget from "@/components/BaseComponents/widgets/EthWidget.vue";
import UsdtWidget from "@/components/BaseComponents/widgets/UsdtWidget.vue";
import UsdcWidget from "@/components/BaseComponents/widgets/UsdcWidget.vue";

export default {
  name: "HomeSection15",
  data() {
    return {
      screen: "crypto",
    };
  },
  methods: {
    changeScreen() {
      this.screen = "crypto"
    },
    changeScreen2() {
      this.screen = "forex"
    },
    changeScreen3() {
      this.screen = "stocks"
    },
  },
  components: {
    UsdcWidget,
    UsdtWidget,
    EthWidget,
    BtcWidget, ChfWidget, JypWidget, GbpWidget, EuroWidget, MetaWidget, GoogleWidget, AppleWidget, NvdaWidget},
}
</script>


<style scoped>

.alpha{
  padding-top: 7%;
  padding-bottom: 7%;
  background-color: #000021;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
}

.section-header{
  font-size: 17px;
  color: #66667a;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
  padding-bottom: 1%;
}
.section-header-1{
  font-size: 30px;
  color: #ffffff;
  font-weight: bold;
  text-align: center;
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
}
.section-alpha{
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  margin-top: 2%;
  gap: 15px;
}

.section-navigation{
  display: flex;
  justify-content: center;
  margin-top: 2%;
  gap: 40px;
}

.nav-item{
  color: #ffffff;
  font-size: 20px;
  font-family: 'BR-Firma-Bold', sans-serif;
}



@media (max-width: 700px) {
  .section-header{
    font-size: 16px;
    margin-left: 8%;
    margin-right: 8%;
  }
  .section-header-1{
    font-size: 28px;
  }
  .section-alpha{
    display: block;
  }
}


@media (max-width: 500px) {

  .section-header-1{
    width: 90%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

}
</style>
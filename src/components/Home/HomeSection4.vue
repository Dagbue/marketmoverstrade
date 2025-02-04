<template>

    <div class="alpha">

      <div class="header">
        <p class="text-1">Trade assets from global markets.</p>
        <p class="text-2">Trade the most popular markets with over 35+ assets available.</p>
      </div>
      <div class="header-select">
        <p @click="changeScreen" class="btn">Cryptos</p>
        <p @click="changeScreen2" class="btn">Forex</p>
        <p @click="changeScreen3" class="btn">Stocks</p>
      </div>

      <crypto-table v-show="this.screen === 'crypto'"/>

      <forex-table v-show="this.screen === 'forex'"/>

      <stock-table v-show="this.screen === 'stocks'"/>

    </div>

</template>

<script>
import CryptoTable from "@/components/BaseComponents/tables/CryptoTable.vue";
import ForexTable from "@/components/BaseComponents/tables/ForexTable.vue";
import StockTable from "@/components/BaseComponents/tables/StockTable.vue";

export default {
  name: "HomeSection4",
  components: {StockTable, ForexTable, CryptoTable},
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
  }
}
</script>

<style scoped>
/*.alpha{*/
/*  margin-top: 3%;*/
/*  margin-bottom: 5%;*/
/*}*/

.alpha{
  background-image: url("@/assets/backgroungimage.png");
  /*background-color: #000;*/
  height: 100%;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding-bottom: 5%;
  padding-top: 5%;
}

.header-select{
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-bottom: 1%;
}

.btn{
  background: linear-gradient(180deg, #3179FF 0%, #1450C8 100%);
  border: 1px solid #3179FF;
  color: #ffffff;
  padding: 0.6em 40px 0.5em 40px;
  border-radius: 12px;
  position: relative;
  display: inline-block;
  margin: 0;
  text-decoration: none;
  -webkit-transition: all 0.1s ease;
  transition: all 0.25s ease;
}
/*.btn:hover{*/
/*  background-color: #ffcf01;*/
/*  border: 1px solid #ffcf01;*/
/*  color: #FFFFFF;*/
/*}*/

.text-1{
  font-size: 28px;
  text-align: center;
  color: #071333;
  padding-bottom: 15px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.text-2{
  font-size: 18px;
  text-align: center;
  color: #0f171c;
  margin-bottom: 3%;
}

.header{
  width: 60%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

@media (max-width: 990px) {

}

@media (max-width: 700px){

  .header{
    width: 95%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .text-1{
    font-size: 24px;
    padding-bottom: 20px;
  }

  .text-2{
    font-size: 16px;
  }

  .header-select{
    gap: 5px;
    margin-top: 3%;
    margin-bottom: 5%;
  }

  .btn{
    padding: 0.5em 30px 0.4em 30px;
  }

}

@media (max-width: 500px){

}

</style>
<template>
  <div class="alpha">

    <div class="section-alpha">

      <div class="section-1">
        <p class="text-1">Empowering our Customers since 2014</p>
        <p class="text-2">We live and breathe the markets. Since the turn of the century, we've  educated traders on what, how,
          and why to trade to help them realize their ambitions.</p>

        <div class="button-group">
          <div class="btn-1" @click="onPostClick">
            Open Account
          </div>
          <div class="btn-1" @click="onPostClick2">
            LogIn
          </div>
        </div>
      </div>

      <div class="section-2">

        <div class="section-2-inner">
          <div class="box">
            <img src="@/assets/Icon-trade.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">Elite products, value, and execution</p>
            <p class="box-text-2">Choose from 80 products and selected futures through our affiliate.
              Enjoy consistently low trading costs and fast, quality execution.</p>

            <p class="box-text-3">TRADE MARKETS</p>
          </div>
          <div class="box">
            <img src="@/assets/Icon-tools.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">Tools designed for your edge</p>
            <p class="box-text-2">Refine your trading with exclusive data tools, Performance Analytics.
              Automate your trading strategies with ease. And take full command of your analysis.</p>

            <p class="box-text-3">TRADING TOOLS</p>
          </div>
        </div>

        <div class="section-2-inner">
          <div class="box">
            <img src="@/assets/customer-support.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">A superior customer experience</p>
            <p class="box-text-2">Access knowledgeable customer support by email or chat, enjoy convenient
              online account management tools, and experience a personalized service.</p>

            <p class="box-text-3">CUSTOMER SUPPORT</p>
          </div>
          <div class="box">
            <img src="@/assets/Icon-Market.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">A trusted global leader</p>
            <p class="box-text-2">We're a wholly-owned, a Fortune 100 financial giant with
              revenues exceeding $54 billion. We're regulated and financially stable.</p>

            <p class="box-text-3">FINANCIAL SECURITY</p>
          </div>
        </div>

      </div>

    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection10",
  methods: {
    onPostClick() {
      this.$router.push("/register");
    },
    onPostClick2() {
      this.$router.push("/login");
    },
  }
}
</script>

<style scoped>
.alpha{
  background-color: #070e20;
  height: 100%;
  padding-top: 10%;
  padding-bottom: 5%;
}

.section-alpha{
  display: flex;
}

.section-1{
  width: 50%;
  margin-left: 3%;
}

.section-2{
  width: 50%;
}

.section-2-inner{
  display: flex;
}

.btn-1{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  height: 46px;
  padding: 8px 16px;
  border-radius: 12px;
  gap: 8px;
  background: linear-gradient(180deg, #3179FF 0%, #1450C8 100%);
  border: 1px solid #3179FF;
  width: 160px;
  /*margin-left: auto;*/
  /*margin-right: auto;*/
  color: #FFFFFF;
  /*margin-bottom: 30px;*/
}
.button-group{
  display: flex;
  justify-content: left;
  gap: 10px;
}

.text-1{
  font-size: 34px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 40px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 8px;
  color: #FFFFFF;
}

.text-2{
  font-size: 17px;
  line-height: 23px;
  letter-spacing: -0.015em;
  text-align: left;
  color: #7A849D;
  margin-bottom: 24px;
}

.box {
  display: flex;
  flex-direction: column;
  border: 1px solid #fff;
  padding: 20px;
  border-radius: 10px;
  color: #fff;
  width: 400px;
  height: 100%;
  margin-bottom: 20px;
  margin-right: 20px;
}

.box-image{
  width: 20%;
}

.box-text-1{
  font-size: 28px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 30px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-top: 40px;
  margin-bottom: 25px;
  color: #FFFFFF;
}

.box-text-2{
  font-size: 15px;
  line-height: 25px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 50px;
  color: #7A849D;
}


.box-text-3{
  font-family: 'BR-Firma-Bold', sans-serif;
}

@media (max-width: 990px){

  .alpha{
    padding-top: 15%;
    padding-bottom: 15%;
  }

  .section-alpha{
    display: block;
  }

  .section-1{
    width: 100%;
    margin-left: unset;
  }

  .section-2{
    width: 100%;
  }

  .text-1{
    font-size: 30px;
    line-height: 30px;
    text-align: center;
  }

  .text-2{
    font-size: 15px;
    line-height: 20px;
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
    text-align: center;
  }

  .button-group{
    display: flex;
    justify-content: center;
    gap: 10px;
  }

  .section-2{
    margin-top: 10%;
  }
}

@media (max-width: 700px){
  .section-2-inner{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .box{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
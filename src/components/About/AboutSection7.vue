<template>
  <div class="alpha">
    <p class="section-header-1">Trade on the world index market with Market Movers Trade.</p>
<!--    <p class="section-header">You decide what to trade and when to trade it. We’re hard at work behind the scenes to-->
<!--      minimize your costs and improve your execution.</p>-->


    <div class="section-alpha">

      <div class="section-2">

        <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/md_exness_indices_trading_ccb60a24d3.jpg" alt="image" class="image" />

      </div>


      <div class="section-1">

        <div class="text-part">
          <p class="text-1">Diversify your portfolio</p>
          <p class="text-2">and gain exposure to the global market by trading stock index derivatives.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Access the most highly-traded major indices</p>
          <p class="text-2">from top markets around the world, including the US, UK, China, Germany, and Japan, with ultra-fast execution and low and stable spreads.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Enjoy immediate access to your earnings</p>
          <p class="text-2">from indices trading with one of the only brokers in the industry to process withdrawals instantly.</p>
        </div>


      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection7"
}
</script>

<style scoped>
.alpha{
  background-color: #ffffff;
  height: 100%;
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding-bottom: 5%;
  padding-top: 3%;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
}

.section-header{
  font-size: 17px;
  color: #0f171c;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
  padding-bottom: 1%;
}
.section-header-1{
  font-size: 28px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
  width: 50%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}
.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  margin-top: 3%;
}

.image{
  width: 75%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  border-radius: 12px;
}

.text-part{
  width: 80%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 3%;
}

.text-1{
  font-size: 26px;
  line-height: 24px;
  font-weight: 500;
  white-space: pre-line;
  margin-bottom: 10px;
  color: #0f171c;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.text-2{
  margin: 0;
  color: #222222;
  font-size: 17px;
  white-space: pre-line;
  line-height: 1.4;
}

@media (max-width: 700px) {
  .section-header{
    font-size: 16px;
    margin-left: 8%;
    margin-right: 8%;
  }
  .section-header-1{
    font-size: 28px;
    width: 90%;
    display: block;
    margin-right: auto;
    margin-left: auto;
  }
  .section-alpha{
    display: block;
  }
  .section-1{
    width: 100%;
  }

  .section-2{
    width: 100%;
    margin-bottom: 5%;
  }

  .text-1{
    font-size: 26px;
    line-height: 24px;
    margin-bottom: 13px;
  }

  .text-2{
    font-size: 16px;
    line-height: 1.3;
  }
  .image{
    width: 90%;
  }
}


@media (max-width: 500px) {
  .text-part{
    width: 85%;
  }

  .section-header-1{
    width: 90%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
<template>
  <div class="alpha">

    <div class="section-alpha">

      <div class="section-1">
        <div class="text-1">Invest in stocks,<br/>
          from local to global</div>

        <p class="text-2">Get the advantages of a local broker on a global investment platform,<br class="breaker"/> with over 6,000 stocks
          to choose from 20 exchanges .</p>


        <div class="button-group">
          <div class="btn-1" @click="onPostClick">
            Start Trading
          </div>
<!--          <div class="btn-1" @click="onPostClick2">-->
<!--            LogIn-->
<!--          </div>-->
        </div>
      </div>

      <div class="section-2">
        <img src="@/assets/Stocks-Cover-960.png" alt="" class="image" />
<!--        <video autoplay="" muted="" loop="">-->
<!--          <source src="https://margex.com/videos/header_mobile_video.mp4" type="video/mp4">-->
<!--        </video>-->
      </div>

    </div>

<!--    <iframe  scrolling="no" allowtransparency="true" frameborder="0" src="https://www.tradingview-widget.com/embed-widget/ticker-tape/#%7B%22colorTheme%22%3A%22light%22%2C%22width%22%3A%22100%25%22%2C%22height%22%3A46%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22ticker-tape%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeCrypto%22%7D" title="ticker tape TradingView widget" lang="en" style="user-select: none; box-sizing: border-box; display: block; height: 65px; width: 100%;"></iframe>-->

  </div>
</template>

<script>
export default {
  name: "HeroSection",
  data() {
    return {
      currentIndex: 0,
      items: [
        { name: 'Forex', color: '#009688' },  // Red
        { name: 'RealEstate', color: '#984613' }  ,  // Yellow
        { name: 'Crypto', color: '#3071EE' }, // Green
        { name: 'Stocks', color: '#5d78ff' }, // Blue
        { name: 'CFD', color: '#fe9431' }    // Yellow
      ],
      intervalId: null
    };
  },
  mounted() {
    this.startRotation();
  },
  beforeDestroy() {
    clearInterval(this.intervalId);
  },
  methods: {
    startRotation() {
      this.intervalId = setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % this.items.length;
      }, 2000); // Change item every 2000 milliseconds
    },
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
  height: 530px;
}
.section-alpha{
  height: 100%;
  display: flex;
  align-items: center;
  align-content: center;
  /* background-image: url("https://margex.com/images/bg_desk.webp");
   background-position: bottom;
   background-repeat: no-repeat;
   background-size: cover;
   position: relative;
  display: block;
  text-align: center;
  margin-left: auto;
  margin-right: auto;*/
 }
 .items-switch .active {
   display: inline; /* Show only active item */
}
.items-switch .active {
  display: inline; /* Show only active item */
}

.items-switch span {
  display: none; /* Hide all by default */
}

.section-1{
  width: 50%;
  margin-left: 5%;
}

.section-2{
  width: 50%;
  margin-right: 1%;
  /*margin-bottom: -10px;
  width: 255px;
  height: 500px;
  background: url("https://margex.com/images/phone_border.svg");
  background-repeat: no-repeat;
  -webkit-background-position: center;
  background-position: center;
  -webkit-background-size: contain;
  background-size: contain;
  padding: 12px 16px 0;
  margin-top: 2%;
  display: block;
  margin-left: auto;
  margin-right: auto;*/
}

video{
  width: 100%;
  border-radius: 30px;
}
.text-1{
  font-size: 40px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 40px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 8px;
  color: #000021;
}

.text-2{
  font-size: 17px;
  line-height: 22px;
  letter-spacing: -0.015em;
  text-align: left;
  color: #7A849D;
  margin-bottom: 24px;
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
  background: #000021;
  border: 1px solid #000021;
  width: 180px;
  /*margin-left: auto;*/
  /*margin-right: auto;*/
  color: #FFFFFF;
  /*margin-bottom: 30px;*/
}

.image{
  width: 100%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.button-group{
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {

  .section-alpha{
    height: 100%;
    padding-top: 5%;
    padding-bottom: 5%;
  }

  .section-alpha{
    display: block;
  }

  .section-1{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .text-1{
    font-size: 43px;
    line-height: 40px;
    margin-bottom: 8px;
    text-align: center;
  }

  .text-2{
    font-size: 15px;
    line-height: 22px;
    text-align: center;
  }

  .btn-1{
    height: 40px;
    padding: 8px 16px;
    gap: 6px;
    width: 160px;
    font-size: 14px;
  }

  .button-group{
    display: flex;
    justify-content: center;
    gap: 12px;
  }

  .section-2{
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 5%;
    width: 100%;
  }

  .section-1{
    width: 100%;
  }

  video{
    width: 100%;
    border-radius: 30px;
  }

  .image{
    width: 100%;
  }

  .breaker{
    display: none;
  }
}

@media (max-width: 500px) {
  .text-1{
    font-size: 30px;
    line-height: 35px;
    margin-bottom: 9px;
  }

  .text-2{
    width: 85%;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
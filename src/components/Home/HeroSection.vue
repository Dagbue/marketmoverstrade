<template>
  <div class="alpha">

    <div class="section-alpha">

      <div class="section-1">
        <div class="text-1">Building Wealth<br/> Through  Diversified <br/> Investments In
<!--          <span class="items-switch">-->
<!--            <span class="forex">Forex</span>-->
<!--            <span class="crypto">Crypto</span>-->
<!--            <span class="stocks">Stocks</span>-->
<!--            <span class="bond">Bond</span>-->
<!--          </span>-->
          <span class="items-switch">
            <span v-for="(item, index) in items" :key="item.name" :class="{active: currentIndex === index}" :style="{ color: item.color }">
              {{ item.name }}
            </span>
          </span>
        </div>

        <p class="text-2">Partner with a trusted global broker and <br/> enjoy access to better-than-market conditions.</p>


        <div class="button-group">
          <div class="btn-1" @click="onPostClick">
            Get Started
<!--            <img src="@/assets/arrow-right-line.svg" alt="" class="" />-->
          </div>
          <div class="btn-1" @click="onPostClick2">
            LogIn
<!--            <img src="@/assets/arrow-right-line.svg" alt="" class="" />-->
          </div>
        </div>
      </div>

      <div class="section-2">
<!--        <img src="@/assets/iphonex.png" alt="" class="image" />-->
        <video autoplay="" muted="" loop="">
          <source src="https://margex.com/videos/header_mobile_video.mp4" type="video/mp4">
        </video>
      </div>


    </div>

    <iframe  scrolling="no" allowtransparency="true" frameborder="0" src="https://www.tradingview-widget.com/embed-widget/ticker-tape/#%7B%22colorTheme%22%3A%22light%22%2C%22width%22%3A%22100%25%22%2C%22height%22%3A46%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22ticker-tape%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeCrypto%22%7D" title="ticker tape TradingView widget" lang="en" style="user-select: none; box-sizing: border-box; display: block; height: 65px; width: 100%;"></iframe>


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
.section-alpha{
  background-image: url("https://margex.com/images/bg_desk.webp");
  background-color: #cccccc;
  height: 600px;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
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
.section-alpha{
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  gap: 20%;
  /*flex-direction: column;*/
}

.section-1{
  /*margin-top: 50px;*/
}

.section-2{
  /*margin-bottom: -10px;*/
  width: 255px;
  height: 500px;
  background: url("https://margex.com/images/phone_border.svg");
  background-repeat: no-repeat;
  -webkit-background-position: center;
  background-position: center;
  -webkit-background-size: contain;
  background-size: contain;
  padding: 12px 16px 0;
}

video{
  width: 100%;
  border-radius: 30px;
}
.text-1{
  font-size: 46px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 64px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 8px;
  color: #FFFFFF;
}

.text-2{
  font-size: 18px;
  line-height: 24px;
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
  background: linear-gradient(180deg, #3179FF 0%, #1450C8 100%);
  border: 1px solid #3179FF;
  width: 160px;
  /*margin-left: auto;*/
  /*margin-right: auto;*/
  color: #FFFFFF;
  /*margin-bottom: 30px;*/
}

.image{
  width: 65%;
  display: block;
  /*margin-left: auto;*/
  margin-right: auto;
  margin-left: 35%;
}


.button-group{
  display: flex;
  justify-content: left;
  gap: 10px;
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
    line-height: 45px;
    margin-bottom: 8px;
    /*width: 90%;*/
    /*margin-left: auto;*/
    /*margin-right: auto;*/
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
  }

  video{
    width: 100%;
    border-radius: 30px;
  }
}

@media (max-width: 500px) {
  .text-1{
    font-size: 35px;
    line-height: 40px;
    margin-bottom: 9px;
  }



  .text-2{
    width: 85%;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
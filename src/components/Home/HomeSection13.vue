<template>
  <div class="alpha">

    <p class="header">Invest with the best</p>

    <p class="sub-header">Join Market Movers and discover why millions have chosen our award-winning platform to start
      investing in stocks</p>

    <div class="section-alpha">

      <div class="section-1">
        <img src="https://www.etoro.com/wp-content/uploads/2025/03/finder_share_mobile.png" alt="" class="image"/>
        <p class="text-1">Award-Winning Platform</p>
        <p class="text-2">Winner of Finder’s 2023 Award for Share Trading – US Stocks</p>
      </div>

      <div class="section-1">
        <img src="https://www.etoro.com/wp-content/uploads/2024/12/BrokerChooser-Winner-Logo.png" alt="" class="image"/>
        <p class="text-1">BrokerChooser Award 2024</p>
        <p class="text-2">Recognized as the Best Stock Trading App</p>
      </div>

      <div class="section-1">
        <img src="https://www.etoro.com/wp-content/uploads/2024/12/Forbes-Winner-Logo.png" alt="" class="image"/>
        <p class="text-1">Forbes Advisor Best of 2024</p>
        <p class="text-2">Best Trading Platform for Day Trading</p>
      </div>

    </div>

    <div class="button-group">
      <div class="btn-1" @click="onPostClick">
        Join Now
      </div>
      <!--          <div class="btn-1" @click="onPostClick2">-->
      <!--            LogIn-->
      <!--          </div>-->
    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection13",
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
  padding-bottom: 5%;
  padding-top: 5%;
  background-color: #f7f7f7;
}


.header{
  text-align: center;
  font-size: 28px;
  font-family: 'BR-Firma-Bold', sans-serif;
  margin-bottom: 5px;
}

.sub-header{
  text-align: center;
  font-size: 18px;
  width: 60%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 3%;
}

.section-1{
  box-shadow: 1px 1px 12px rgba(0,0,0,.1);
  background-color: #FFFFFF;
  max-width: 260px;
  min-width: min(100% - 40px, 260px);
  width: 100%;
  border-radius: 20px;
  margin: 0;
  overflow: hidden;
  padding: 16px 24px 20px;
}

.text-1{
  font-size: 22px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 24px;
  margin-bottom: 15px;
  margin-top: 0;
}

.text-2{
  color: #66667a;
  font-size: 16px;
  line-height: 26px;
  margin-bottom: 30px;
}

.section-alpha{
  display: flex;
  justify-content: center;
  gap: 25px;
}

.bx{
  color: #000021;
  font-size: 50px;
  margin-bottom: 28px;
  margin-top: 15px;
}

.image{
  width: 100%;
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
  width: 200px;
  /*margin-left: auto;*/
  /*margin-right: auto;*/
  color: #FFFFFF;
  /*margin-bottom: 30px;*/
}



.button-group{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  margin-top: 3%;
}


@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .section-alpha{
    display: block;
  }

  .sub-header{
    width: 90%;
  }

  .section-1{
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 5%;
  }
}

@media (max-width: 500px) {
  .section-1{
    max-width: 280px;
  }
}

</style>
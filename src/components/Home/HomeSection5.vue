<template>
  <div class="alpha">
    <div class="section-1-alpha">
      <div class="section-1">
        <p class="text-1">Join Market Movers Trade and experience greatness</p>
        <p class="text-2">
          Discover the power of Market Movers Trade, a cutting-edge platform that integrates cryptocurrency, stocks, and
          forex trading. Seamlessly manage and trade across these markets from a single platform, offering both
          convenience and control for your financial portfolio.</p>
<!--        <p class="text-2">Download the Rubies app</p>-->
                <div class="btn-part">
                  <div class="btn-1" @click="onPostClick">Create Account</div>
                  <p class="btn-2" @click="onPostClick2">Log In</p>
                </div>
<!--        <div class="play-store">-->
<!--          <img src="@/assets/applestore.svg" alt="" class="store-image" />-->
<!--          <img src="@/assets/gogleplay.svg" alt="" class="store-image" />-->
<!--        </div>-->
      </div>

      <div class="image-section">
<!--        <img src="@/assets/aaaaa.png" alt="" class="image"/>-->
        <video autoplay="" muted="" loop="" class="css-1bywlvb">
          <source src="https://margex.com/videos/ct_land.mp4" type="video/mp4">
        </video>
      </div>
    </div>



  </div>
</template>

<script>
export default {
  name: "HomeSection5",
  methods: {
    onPostClick() {
      this.$router.push("/register");
    },
    onPostClick2() {
      this.$router.push("/login");
    },
  },
}
</script>

<style scoped>

.alpha{
  /*background-image: url("@/assets/background.png");*/
  /*background-color: #000;*/
  height: 100%;
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  background-color: #070e20;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.css-1bywlvb {
  background: url("https://margex.com/images/tablet_square_border.svg");
  background-repeat: no-repeat;
  -webkit-background-position: center;
  background-position: center;
  -webkit-background-size: contain;
  background-size: contain;
  padding: 10px;
  border-radius: 30px;
  max-width: 563px;
  height: auto;
}

.section-1{
  /*margin-top: 75px;*/
  width: 50%;
  margin-left: 10%;
}

.image-section{
  width: 50%;
  margin-right: 4%;
}

.image{
  width: 100%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.section-1-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  padding-top: 5%;
  padding-bottom: 3%;
}

.text-1{
  font-size: 45px;
  line-height: 50px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 10px;
  color: #FFFFFF;
  font-family: 'BR-Firma-Bold', sans-serif;
  width: 85%;
}

.text-2{
  font-size: 17px;
  line-height: 24px;
  letter-spacing: -0.015em;
  text-align: left;
  color: #7A849D;
  margin-bottom: 15px;
  width: 80%;
}


.play-store{
  display: flex;
  gap: 20px;
}

span{
  padding: 3px 15px;
  align-items: center;
  gap: 4px;
  background-color: #EFFAF6;
  color: #2D9F75;
  border-radius: 100px;
  margin-left: 5px;
}

.btn-part{
  display: flex;
  gap: 15px;
}

.btn-1{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  height: 48px;
  padding: 8px 16px;
  border-radius: 14px;
  gap: 8px;
  background-color: transparent;
  border: 1px solid #d0d0d0;
  color: #ffffff;
  width: 180px;
}

.btn-2{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  height: 48px;
  padding: 8px 16px;
  border-radius: 14px;
  gap: 8px;
  background: linear-gradient(180deg, #3179FF 0%, #1450C8 100%);
  border: 1px solid #3179FF;
  width: 180px;
  color: #ffffff;
}

video{
  width: 100%;
}
@media (max-width: 990px) {
}

@media (max-width: 700px) {

  .text-1{
    font-size: 45px;
    line-height: 50px;
    margin-bottom: 8px;
    text-align: center;
    margin-top: 5%;
    display: block;
    margin-right: auto;
    margin-left: auto;
  }

  .text-2{
    font-size: 17px;
    line-height: 22px;
    text-align: center;
    width: 90%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .section-1-alpha{
    display: flex;
    flex-direction: column-reverse;
    justify-content: space-around;
    align-items: center;
    align-content: center;
    padding-top: 8%;
    padding-bottom: 8%;
  }

  .section-1{
    width: 100%;
    margin-left: unset;
  }

  .image-section{
    width: 90%;
    display: block;
    margin-right: auto;
    margin-left: auto;
  }

  .btn-part{
    display: flex;
    justify-content: center;
    gap: 15px;
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

  .btn-part{
    display: flex;
    justify-content: center;
    gap: 15px;
  }
}
</style>
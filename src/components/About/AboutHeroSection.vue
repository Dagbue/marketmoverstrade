<template>
  <div class="alpha">
<!--    <p class="section-header-1">There’s a time and a place for risk</p>-->
<!--    <p class="section-header">Your funds and data are always secure. With Income And Assets Limited you’re protected-->
<!--      by industry-leading protocols.</p>-->

    <div class="section-alpha">

      <div class="section-1">

        <div class="text-part">
          <p class="text-3">Market Movers Trade</p>
          <p class="text-1">Investing. Now available <br/> to everyone.</p>
          <p class="text-2">we see investing differently. Today’s financial system is complex, exclusive and
            expensive - making it hard for the typical person to start investing.So, we’re building a platform without
            digital walls and complex barriers. A platform that empowers you to see new possibilities for your money
            - and helps make them a reality.</p>

<!--          <div class="button-part">-->
<!--            <button class="btn1" @click="onPostClick2">Login Account</button>-->
<!--          </div>-->
        </div>


      </div>

      <div class="section-2">

        <img src="@/assets/pick.webp" alt="image" class="image" />

      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "AboutHeroSection",
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
  background-color: #000021;
  height: 600px;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

span{
  color: #3071EE;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
}

.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  padding-top: 3.5%;
}

.image{
  width: 80%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  border-radius: 14px;
}

.text-part{
  width: 80%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.text-1{
  font-size: 40px;
  line-height: 1;
  white-space: pre-line;
  margin-bottom: 10px;
  font-family: 'BR-Firma-Bold', sans-serif;
  color: #FFFFFF;
}

.text-2{
  margin: 0;
  font-size: 18px;
  white-space: pre-line;
  line-height: 1.15;
  color: #7A849D;
}

.text-3{
  background: linear-gradient(180deg, #3179FF 0%, #1450C8 100%);
  border: 1px solid #3179FF;
  display: inline-block;
  color: #FFFFFF;
  padding: 6px 30px 4px 30px;
  border-radius: 12px;
  margin-bottom: 2%;
  /*font-family: 'BR-Firma-Light', sans-serif;*/
}

.button-part{
  display: flex;
  gap: 20px;
  margin-top: 3%;
}
.btn1{
  background-color: #070e20;
  border: 1px solid #070e20;
  color: #ffffff;
  padding: 10px 30px;
  border-radius: 12px;
  position: relative;
  display: inline-block;
  margin: 0;
  text-decoration: none;
  -webkit-transition: all 0.1s ease;
  transition: all 0.25s ease;
  font-size: 14px;
  width: 220px;
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
  .section-1{
    width: 100%;
  }

  .section-2{
    width: 100%;
  }

  .text-1{
    font-size: 28px;
    line-height: 30px;
    margin-bottom: 13px;
    display: block;
    margin-right: auto;
    margin-left: auto;
    text-align: center;
  }

  .text-2{
    font-size: 16px;
    line-height: 1.3;
    display: block;
    margin-right: auto;
    margin-left: auto;
    text-align: center;
  }

  .text-3{
    display: block;
    margin-right: auto;
    margin-left: auto;
    text-align: center;
  }

  .image{
    width: 80%;
  }

  .button-part{
    justify-content: center;
  }
  .alpha{
    padding-top: 10%;
    padding-bottom: 10%;
    height: 100%;
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
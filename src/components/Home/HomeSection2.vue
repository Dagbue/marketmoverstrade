<template>
  <div class="alpha">

    <div class="section-1">
      <h2 class="text-1" style="text-align: center;"> Market Movers Trade is More than Just <br/> a Trading Platform</h2>
      <p class="text-2">Give your trading strategy the advantage with our better-than-market conditions.</p>
    </div>


    <div  class="section-1-inner">

      <div class="section-1-inner-content">
        <img src="@/assets/products_staking.svg" alt="" class="image"/>
        <br/>
        <h1>Staking</h1>
        <p class="description">Earn staking rewards on your crypto in addition to your trading.</p>
      </div>

      <div class="section-1-inner-content">
        <img src="@/assets/products_copy.svg" alt="" class="image"/>
        <br/>
        <h1>Referral</h1>
        <p class="description">Up to 5% commission from your referrals! One of the best programs in the industry.</p>
      </div>

      <div class="section-1-inner-content">
        <img src="@/assets/products_alerts.svg" alt="" class="image"/>
        <br/>
        <h1>Price Alerts</h1>
        <p class="description">Stay in touch with all important market movements and price changes to take control
          of your trading opportunities.</p>
      </div>

    </div>

    <div class="btn-part">
      <div class="btn-1" @click="onPostClick">Create Account</div>
      <p class="btn-2" @click="onPostClick2">Log In</p>
    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection2",
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
  padding-top: 5%;
  padding-bottom: 5%;
  background: #070e20;

}

.section-1-inner{
  display: flex;
  margin-top: 4%;
}

.section-1-inner-content{
  text-align: center;
  width: 46%;
}
.section-1-inner-content h1{
  font-size: 18px;
  font-family: 'BR-Firma-Bold', sans-serif;
  padding-bottom: 5px;
  color: #FFFFFF;
}

.description{
  width: 75%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  color: #7A849D;
}

.description-2{
  width: 55%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.image{
  display: block;
  margin-left: auto;
  margin-right: auto;
  object-fit: cover;
  width: 150px;
}

.image-2{
  display: block;
  margin-left: auto;
  margin-right: auto;
  object-fit: cover;
  width: 65px;
}

.text-1{
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 28px;
  padding-bottom: 10px;
  font-family: 'BR-Firma-Bold', sans-serif;
  color: #FFFFFF;
}
.text-2{
  font-size: 18px;
  text-align: center;
  padding-bottom: 1%;
  color: #7A849D;
}
.bx{
  font-size: 30px;
  margin-top: 10px;
}

.image-part{
  display: flex;
  justify-content: center;
  margin-top: 15px;
  gap: 20px;
}

.btn-part{
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 3%;
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
  color: #d0d0d0;
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


@media (max-width: 990px){

  .image{
    width: 100%;
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-top: 3%;
  }


  .alpha{
    padding-top: 10%;
    padding-bottom: 10%;
  }

  .text-1{
    width: 90%;
  }

  .section-1-inner{
    display: block;
  }

  .image{
    display: block;
    margin-left: auto;
    margin-right: auto;
    object-fit: cover;
    width: 180px;
  }

  .section-1-inner-content{
    text-align: center;
    width: 100%;
  }

  .btn-part{
    margin-top: 5%;
  }

}

@media (max-width: 500px){

  .section-1-inner{
    display: block;
  }

  .image{
    display: block;
    margin-left: auto;
    margin-right: auto;
    object-fit: cover;
    width: 180px;
  }

  .text-2{
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
  }
}
</style>
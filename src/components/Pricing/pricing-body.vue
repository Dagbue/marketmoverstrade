<template>
<div class="alpha">

  <div class="section-alpha-1">
    <p class="section-header-1">Choose an Investment Plan</p>
    <p class="section-header">You don't have an account yet? start trading with Market Movers Trade. </p>
  </div>

  <div class="section-alpha">

    <div class="third-section top">
      <p class="text-1">Silver</p>
      <p class="text-2">5<span class="text-2-inner">%</span></p>
      <!--        <p class="text-2">4 Months</p>-->
      <p class="text-3">4 Months</p>

      <div class="btn" @click="onPostClick" >
        <p>Invest Now</p>
      </div>

      <div class="separate">
        <p>$5,000 MINIMUM DEPOSIT</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>ENHANCED SECURITY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>1.2% DAILY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>GUARANTEED ROI</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>24/7 SUPPORT</p>
        <i class='bx bxs-info-circle'></i>
      </div>
    </div>

    <div class="third-section top">
      <p class="text-1">Gold</p>
      <p class="text-2">10<span class="text-2-inner">%</span></p>
      <!--        <p class="text-2">4 Months</p>-->
      <p class="text-3">8 Months</p>

      <div class="btn" @click="onPostClick" >
        <p>Invest Now</p>
      </div>

      <div class="separate">
        <p>$25,000 MINIMUM DEPOSIT</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>ENHANCED SECURITY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>1.4% DAILY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>GUARANTEED ROI</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>24/7 SUPPORT</p>
        <i class='bx bxs-info-circle'></i>
      </div>
    </div>

    <div class="third-section top">
      <p class="text-1">Diamond</p>
      <p class="text-2">15<span class="text-2-inner">%</span></p>
      <!--        <p class="text-2">4 Months</p>-->
      <p class="text-3">12 Months</p>

      <div class="btn" @click="onPostClick" >
        <p>Invest Now</p>
      </div>

      <div class="separate">
        <p>$100,000 MINIMUM DEPOSIT</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>ENHANCED SECURITY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>1.6% DAILY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>GUARANTEED ROI</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>24/7 SUPPORT</p>
        <i class='bx bxs-info-circle'></i>
      </div>
    </div>

    <div class="third-section top">
      <p class="text-1">Platinum</p>
      <p class="text-2">20<span class="text-2-inner">%</span></p>
      <!--        <p class="text-2">4 Months</p>-->
      <p class="text-3">24 Months</p>

      <div class="btn" @click="onPostClick" >
        <p>Invest Now</p>
      </div>

      <div class="separate">
        <p>$250,000 MINIMUM DEPOSIT</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>ENHANCED SECURITY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>1.8% DAILY</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>GUARANTEED ROI</p>
        <i class='bx bxs-info-circle'></i>
      </div>

      <div class="separate">
        <p>24/7 SUPPORT</p>
        <i class='bx bxs-info-circle'></i>
      </div>
    </div>

  </div>

</div>
</template>

<script>
export default {
  name: "pricing-body",
  methods: {
    onPostClick() {
      this.$router.push("/register");
      window.scrollTo(0, 0);
    },
  },
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
  padding-top: 5%;
}
.section-header{
  font-size: 17px;
  color: #070e20;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
  padding-bottom: 1%;
}
.section-header-1{
  font-size: 30px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
}
.section-alpha{
  display: flex;
  justify-content: space-evenly;
  margin-right: 3%;
  margin-left: 3%;
}

.section-alpha-2{
  display: flex;
  justify-content: space-evenly;
}

.section-alpha-1{
  display: block;
  text-align: center;
  margin-bottom: 2%;
}

.third-section{
  width: 300px;
  height: 480px;
  background-color: #ffffff;
  box-shadow:  20px 20px 60px #d9d9d9,
  -20px -20px 60px #ffffff;
  border-radius: 8px;
  margin-bottom: 5%;
}

.separate{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  margin-top: 1%;
}

.separate i{
  padding-top: 15px;
  padding-right: 13px;
}

.separate p{
  width: 220px;
  padding-top: 15px;
  font-size: 14px;
  line-height: 24px;
  color: #667085;
  padding-left: 13px;
}

.btn{
  margin-top: 5%;
  margin-bottom: 1%;
}

.btn p{
  display: block;
  margin-left: auto;
  margin-right: auto;
  align-items: center;
  padding: 12px 20px;
  gap: 8px;
  width: 180px;
  height: 44px;
  background: #000021;
  border: 1px solid #000021;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 12px;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #FFFFFF;
  text-align: center;
}

/*.btn p:hover{*/
/*  background-color: #ffcf01;*/
/*  color: #ffffff;*/
/*  border: 1px solid #ffcf01;*/
/*  -webkit-transition: all 0.35s ease;*/
/*  transition: all 0.35s ease;*/
/*  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);*/
/*}*/

.top{
  margin-top: 1%;
}

.text-1{
  text-align: center;
  padding-top: 9%;
  padding-bottom: 3%;
  font-size: 19px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.text-2{
  text-align: center;
  padding-bottom: 4%;
  font-size: 27px;
  font-weight: bold;
}

.text-2-inner{
  font-size: 14px;
  font-weight: normal;
}

.text-3{
  text-align: center;
  font-size: 16px;
  width: 70%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}


.bx{
  color: #000021;
}
@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .section-alpha{
    display: block;
    /*margin-left: 21%;*/
    margin-top: 3.5%;
  }
  .section-alpha-2{
    display: block;
    /*margin-left: 21%;*/
    margin-top: 3.5%;
  }
  .third-section{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .section-header{
    margin-left: 10%;
    margin-right: 10%;
  }
  .section-header-1{
    font-size: 25px;
  }

  .third-section{
    width: 350px;
  }
}

@media (max-width: 500px) {

  .third-section{
    width: 300px;
  }
}

</style>
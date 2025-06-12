<template>
  <div class="section-alpha">

<!--    <p class="section-header-1">Trade with confidence</p>-->
<!--    <p class="section-header">The numbers speak for themselves. Trade with the support of the world’s largest-->
<!--      retail broker.</p>-->

    <div class="section-2">
      <div class="section-2-alpha">

        <div class="section-2-content">
          <p class="text-1">Trusted by</p>
          <div class="seprate">
            <i class='bx bx-group'></i>
            <p class="text-2">7M+ people</p>
          </div>
        </div>

        <div class="vl"></div>

        <div class="section-2-content">
          <p class="text-1">Insurance on custodial assets by</p>
          <div class="seprate">
            <img src="@/assets/logo-ledger.svg" alt="" class="section-img">
            <img src="@/assets/logo-fireblocks-white.svg" alt="" class="section-img">
          </div>
        </div>

        <div class="vl"></div>

        <div class="section-2-content">
          <p class="text-1">Operating securely since</p>
          <div class="seprate">
            <i class='bx bxs-award'></i>
            <p class="text-2">2016</p>
          </div>
        </div>

        <div class="vl"></div>

        <div class="section-2-content">
          <p class="text-1">4.6</p>
          <p class="text-2">Trustpilot rating</p>
        </div>

      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: "AboutSection1"
}
</script>

<style scoped>

.seprate{
  display: flex;
  justify-content: center;
  gap: 5px;
  align-content: center;
  align-items: center;
  padding-top: 5px;
}

.section-img{
  padding-right: 10px;
  width: 35%;
}

.bx{
  font-size: 25px;
}

.section-alpha{
  background-color: #f7f7f7;

  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding-bottom: 3%;
  padding-top: 3%;
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
  font-size: 30px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 1%;
  font-family: 'BR-Firma-Bold', sans-serif;
  width: 40%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.box{
  background-color: #ffffff;
  box-shadow:  20px 20px 60px #d9d9d9,
  -20px -20px 60px #ffffff;
  padding: 15px;
  border-radius: 12px;
  margin-bottom: 12px;
  margin-top: 4%;
  width: 330px;
  height: 250px;
}



.section-content-1{
  display: flex;
  justify-content: space-evenly;
}

.bxs-coin-stack{
  text-align: center;
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 60px;
  padding-top: 10px;
}

.bx-timer{
  text-align: center;
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 60px;
  padding-top: 10px;
}

.bxs-calendar-x{
  text-align: center;
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 65px;
  padding-top: 15px;
}

.bx-repost{
  text-align: center;
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 70px;
  padding-top: 15px;
}

.bxs-credit-card{
  text-align: center;
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 70px;
  padding-top: 25px;
}

.bx-euro ,.bx-pound , .bx-yen{
  font-size: 45px;
  padding-top: 25px;
}
.about-image-1{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 30%;
}
.about-image-2{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 37%;
}
.about-image-3{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 29%;
}

.box h3{
  padding-top: 12px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  margin-bottom: 8px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.box p{
  color: #222222;
  text-align: center;
  font-size: 15px;
  line-height: 1.5;
  width: 90%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}


.section-2-alpha{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: space-between;
  /*margin-top: 3%;*/
  /*margin-bottom: 6%;*/
  margin-left: 8%;
  margin-right: 8%;
}

.section-2-content{
  /*margin-right: 40px;*/
  text-align: center;
}

.text-1{
  font-family: 'BR-Firma-Bold', sans-serif;
  font-size: 20px;
  padding-bottom: 3px;
}

.text-2 {
  font-size: 17px;
}

.vl {
  border-left: 1.5px solid rgba(0, 0, 0, 0.12);
  height: 100px;
}

@media (max-width: 700px) {
  .section-header{
    font-size: 15px;
    margin-left: 10%;
    margin-right: 10%;
  }
  .section-content-1{
    display: flex;
    flex-direction: column-reverse;
    justify-content: space-evenly;
  }

  .section-header-1{
    font-size: 26px;
    width: 95%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .box{
    /*margin-left: 10%;*/
    /*margin-right: 10%;*/
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .section-2-alpha{
    display: block;
    /*margin-bottom: 6%;*/
    margin-left: 8%;
    margin-right: 8%;
  }

  .vl {
    display: none;
  }

  .section-2-content{
    padding-bottom: 7%;
  }

  .section-img{
    width: 22%;
  }

}



@media (max-width: 500px) {
  .section-2-alpha{
    margin-top: 7%;
    margin-bottom: 8%;
    margin-left: 2%;
    margin-right: 2%;
  }

  .section-header{
    margin-left: 4%;
    margin-right: 4%;
  }
}
</style>
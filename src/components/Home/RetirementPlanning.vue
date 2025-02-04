<template>
  <div class="alpha">

    <p class="section-header-1">Retirement Planning</p>
    <p class="section-header">
      Secure your future by diversifying investments in cryptocurrencies and traditional assets on a unified
      platform. Enjoy global trading, multi-currency support, and 24/6 market access to make informed retirement
      planning decisions.
    </p>



    <div class="section-alpha">

      <div class="section-2">

        <img src="@/assets/retirement.jpg" alt="image" class="image-2" />

      </div>

      <div class="section-1">

        <div class="text-part">
          <p class="text-1">Diversify for Retirement Security</p>
          <p class="text-2">Build a robust retirement portfolio with a mix of global assets, including popular stocks
            like Alphabet, Boeing, McDonald's, and Nike, alongside cryptocurrencies and more..</p>
        </div>

        <div class="text-part">
          <p class="text-1">Benefit from Consistent Returns</p>
          <p class="text-2">
            Enjoy tight, stable spreads that help you maximize your investments while trading with confidence
            and peace of mind.
          </p>
        </div>

        <div class="text-part">
          <p class="text-1">Seamless Execution for Smarter Investing</p>
          <p class="text-2">
            Take advantage of superior trade execution across Forex, Crypto, CFDs, and Stocks, ensuring you stay
            ahead in your retirement planning strategy.
          </p>
        </div>


      </div>


    </div>

  </div>
</template>

<script>
export default {
  name: "RetirementPlanning"
}
</script>


<style scoped>
/*.alpha{*/
/*  padding-bottom: 5%;*/
/*  padding-top: 5%;*/
/*}*/

.section-2{
  width: 50%;
}

.section-1{
  width: 50%;
}

.alpha{
  background-image: url("@/assets/backgroungimage.png");
  /*background-color: #000;*/
  height: 100%;
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding-bottom: 5%;
  padding-top: 3%;
}

.section-header{
  font-size: 17px;
  color: #0f171c;
  text-align: center;
  font-weight: 300;
  margin-left: 20%;
  margin-right: 20%;
  padding-bottom: 1%;
  line-height: 1.3;
}
.section-header-1{
  font-size: 30px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
  width: 45%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 2%;
}

.cards{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px,1fr));
  padding: 20px;
  grid-gap: 40px;
}

.card{
  background-color: #ffffff;
  box-shadow:  20px 20px 60px #d9d9d9,
  -20px -20px 60px #ffffff;
  border-radius: 8px;
}

.container{
  position: relative;
  clip-path: polygon(0 0,100% 0, 100% 85%, 0 100%);
}

img{
  width: 100%;
  display: block;
  border-radius: 20px 20px 0 0;
}

.card-alpha{
  display: grid;
  margin-left: 10%;
  margin-right: 10%;
  place-items: center center;
}

.container:after{
  content: "";
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  border-radius: 20px 20px 0 0;
  opacity: 0.9;
}

.details{
  padding: 20px 10px;
}



.details>h3{
  color: #0f171c;
  font-weight: 600;
  font-size: 18px;
  margin: 10px 0 15px 0;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.details>p{
  color: #697582;
  font-weight: 400;
  font-size: 15px;
  line-height: 18px;
}

.section-alpha-2{
  margin-bottom: 1%;
}

hr.new1 {
  border-top: 1px solid #676767;
  /*margin-top: 3%;*/
  width: 85%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}
.section{
  display: flex;
  justify-content: space-evenly;
  padding-top: 20px;
  padding-bottom: 20px;
}
.section-inner{
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
}
.text-1-1{
  padding-left: 10px;
}
.image{
  width: 25%;
}

.css-s7y1fb {
  width: 1000px !important;
  height: 524px !important;
  background: url("https://margex.com/images/tablet_border.svg");
  background-repeat: no-repeat;
  -webkit-background-position: center;
  background-position: center;
  -webkit-background-size: contain;
  background-size: contain;
  padding: 10px;
  border-radius: 65px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 1%;
  margin-bottom: 2%;
}

video{
  width: 85%;
}



.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  margin-top: 3%;
  margin-bottom: 4%;
}

.image-2{
  width: 68%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  border-radius: 12px;
}

.text-part{
  width: 75%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 5%;
}

.text-1{
  font-size: 28px;
  line-height: 26px;
  font-weight: 500;
  white-space: pre-line;
  margin-bottom: 10px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.text-2{
  margin: 0;
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
  }

  .section-alpha{
    display: block;
  }
  .cards{
    grid-template-columns: repeat(auto-fit, minmax(300px,1fr));
    grid-gap: 30px;
  }

  .section{
    display: block;
    margin-right: auto;
    margin-left: auto;
    padding-top: 10px;
    padding-bottom: 10px;
  }

  .section-inner{
    /*margin-left: 15%;*/
    margin-bottom: 3%;
  }

  .image{
    width: 8%;
  }

  .section-2{
    width: 100%;
  }

  .section-1{
    width: 100%;
    margin-top: 5%;
  }

  .image-2{
    width: 85%;
  }
}


@media (max-width: 500px) {
  .image{
    width: 13%;
  }


}
</style>
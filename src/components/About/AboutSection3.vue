<template>
  <div class="section-alpha">

    <p class="section-header-1">Trade with confidence</p>
    <p class="section-header">The numbers speak for themselves. Trade with the support of the world’s largest
      retail broker.</p>




    <div class="section-content">

      <div class="section-content-1" >
        <div class="box">
          <img src="https://margex.com/images/products_futures.svg" class="about-image" alt="assets-image"/>
          <h3>Futures</h3>
          <p>Trade cryptocurrency derivatives with the best-in-class UI for both professionals and beginners.</p>
        </div>
        <div class="box">
          <img src="https://margex.com/images/products_copy.svg" class="about-image" alt="assets-image"/>
          <h3>Copy Trading</h3>
          <p>Experience 30% fewer stop outs with a unique protection feature designed to
            delay or completely avoid stop outs.</p>
        </div>
        <div class="box">
          <img src="https://margex.com/images/products_staking.svg" class="about-image" alt="assets-image"/>
          <h3>Staking</h3>
          <p>Over 100 successful traders. Choose and copy 100% of their trades in 1 click.</p>
        </div>
      </div>

      <div class="section-content-1" >
        <div class="box">
          <img src="https://margex.com/images/products_alerts.svg" class="about-image" alt="assets-image"/>
          <h3>Price Alerts</h3>
          <p>Stay in touch with all important market movements and price changes.</p>
        </div>
        <div class="box">
          <img src="https://margex.com/images/products_crypto.svg" class="about-image" alt="assets-image"/>
          <h3>Buy Crypto</h3>
          <p>Purchase cryptocurrency through Market Movers Trade trusted partners.</p>
        </div>
        <div class="box">
          <img src="https://margex.com/images/products_mobile.svg" class="about-image" alt="assets-image"/>
          <h3>Two Mobile Apps</h3>
          <p>"Market Movers Trade app" - For Traders "Copy trading app" - For Followers</p>
        </div>
      </div>


    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection3"
}
</script>

<style scoped>

.section-alpha{
  background-color: #f7f7f7;

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
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.box{
  background-color: #ffffff;
  /*box-shadow:  20px 20px 60px #d9d9d9,*/
  /*-20px -20px 60px #ffffff;*/
  padding: 15px;
  border-radius: 12px;
  margin-bottom: 12px;
  margin-top: 4%;
  width: 330px;
  height: 330px;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}

.section-content-1{
  display: flex;
  justify-content: space-evenly;
}

.about-image{
  display: block;
  margin-left: auto;
  margin-right: auto;
  height: 100px;
  width: 100px;
  object-fit: cover;
  margin-top: 7%;
}


.box h3{
  padding-top: 22px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  margin-bottom: 6px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.box p{
  color: #222222;
  text-align: center;
  font-size: 15px;
  line-height: 1.5;
  padding-top: 5%;
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
}



@media (max-width: 500px) {
  .section-header{
    margin-left: 4%;
    margin-right: 4%;
  }
}
</style>
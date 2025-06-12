<template>
  <div class="alpha">
    <p class="section-header-1">The tools to help you invest smarter</p>
    <p class="section-header">From foundational basics to advanced strategies, Market Movers offers unique features
      that take your portfolio to the next level.</p>


    <div class="section-alpha">

      <div class="section-1">

        <div class="text-part">
          <p class="text-1">Access in-depth analysis</p>
          <p class="text-2">Stay ahead of the curve with pro tools like TradingView charts — all the data you need, in
            user-friendly format.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Tap into the trends</p>
          <p class="text-2">
            Explore today’s top market movers as well as emerging players from leading exchanges all over the globe.
          </p>
          <br/>
          <p class="text-1">Grow your investment skills</p>
          <p class="text-2">Get the knowledge to make better decisions on the daily markets </p>
        </div>

        <div class="text-part">
          <p class="text-1">Go behind the curtain</p>
          <p class="text-2">
            Take a deep dive into the companies making big moves in the markets with our weekly Stock Break podcast.
          </p>
          <br/>
          <p class="text-1">Copy top stock traders</p>
          <p class="text-2">Invest like our best-performing traders with : choose an investor, and when they trade.</p>
        </div>


      </div>

      <div class="section-2">

        <img src="@/assets/phone2n.png" alt="image" class="image" />

      </div>

    </div>

  </div>
</template>


<script>
export default {
name: "HomeSection12"
}
</script>


<style scoped>

.alpha{
  padding-top: 5%;
  padding-bottom: 5%;
  background-color: #000021;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
}

.section-header{
  font-size: 17px;
  color: #66667a;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
  padding-bottom: 1%;
}
.section-header-1{
  font-size: 30px;
  color: #ffffff;
  font-weight: bold;
  text-align: center;
  padding-bottom: 0.5%;
  font-family: 'BR-Firma-Bold', sans-serif;
}
.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  margin-top: 3%;
}

.image{
  width: 70%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.text-part{
  width: 75%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 5%;
}

.text-1{
  font-size: 26px;
  line-height: 26px;
  font-weight: 500;
  white-space: pre-line;
  margin-bottom: 10px;
  font-family: 'BR-Firma-Bold', sans-serif;
  color: #ffffff;
}

.text-2{
  margin: 0;
  font-size: 17px;
  white-space: pre-line;
  line-height: 1.4;
  color: #66667a;
}

@media (max-width: 700px) {
  .section-header{
    font-size: 16px;
    margin-left: 8%;
    margin-right: 8%;
  }
  .section-header-1{
    font-size: 28px;
    padding-top: 6%;
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
    font-size: 26px;
    line-height: 24px;
    margin-bottom: 13px;
  }

  .text-2{
    font-size: 16px;
    line-height: 1.3;
  }
  .image{
    width: 90%;
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
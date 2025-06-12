<template>
  <div class="alpha">

    <p class="header">Why trade with Market Movers <br/> Trade?</p>

    <div class="section-alpha">

<!--      <div class="section-1">-->
<!--        <p class="text-1">Empowering our Customers since 2001</p>-->
<!--        <p class="text-2">We live and breathe the markets. Since the turn of the century, we've  educated traders on what, how,-->
<!--          and why to trade to help them realize their ambitions.</p>-->

<!--        <div class="button-group">-->
<!--          <div class="btn-1" @click="onPostClick">-->
<!--            Open Account-->
<!--          </div>-->
<!--          <div class="btn-1" @click="onPostClick2">-->
<!--            LogIn-->
<!--          </div>-->
<!--        </div>-->
<!--      </div>-->

      <div class="section-2">

        <div class="section-2-inner">
          <div class="box">
            <svg xmlns="http://www.w3.org/2000/svg" width="65" height="65" viewBox="0 0 24 24" fill="none"
                 stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"
                 class="lucide lucide-server n-tile-icon n-tile-icon-icon">
              <rect width="20" height="8" x="2" y="2" rx="2" ry="2"></rect>
              <rect width="20" height="8" x="2" y="14" rx="2" ry="2"></rect>
              <line x1="6" x2="6.01" y1="6" y2="6"></line>
              <line x1="6" x2="6.01" y1="18" y2="18"></line>
            </svg>
            <p class="box-text-1">London-based server</p>
            <p class="box-text-2">Our London based server and industry reputation helps us provide a tier-one liquidity
              solution, so we can consistently deliver lightning-quick execution speeds.</p>

<!--            <p class="box-text-3">TRADE MARKETS</p>-->
          </div>
          <div class="box">
            <svg xmlns="http://www.w3.org/2000/svg" width="65" height="65" viewBox="0 0 24 24" fill="none"
                 stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"
                 class="lucide lucide-user-cog n-tile-icon n-tile-icon-icon"><circle cx="18" cy="15" r="3"></circle>
              <circle cx="9" cy="7" r="4"></circle>
              <path d="M10 15H6a4 4 0 0 0-4 4v2"></path>
              <path d="m21.7 16.4-.9-.3"></path>
              <path d="m15.2 13.9-.9-.3"></path>
              <path d="m16.6 18.7.3-.9"></path>
              <path d="m19.1 12.2.3-.9"></path>
              <path d="m19.6 18.7-.4-1"></path>
              <path d="m16.8 12.3-.4-1"></path>
              <path d="m14.3 16.6 1-.4"></path>
              <path d="m20.7 13.8 1-.4"></path
              ></svg>
            <p class="box-text-1">Unrestricted Trading</p>
            <p class="box-text-2">Our platform have no restrictions on minimum stop-loss or take-profit
              distances and limits, especially useful for high-volume traders.</p>
          </div>
        </div>

        <div class="section-2-inner">
          <div class="box">
            <svg xmlns="http://www.w3.org/2000/svg" width="65" height="65" viewBox="0 0 24 24" fill="none"
                 stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"
                 class="lucide lucide-sliders-vertical n-tile-icon n-tile-icon-icon">
              <line x1="4" x2="4" y1="21" y2="14"></line>
              <line x1="4" x2="4" y1="10" y2="3"></line>
              <line x1="12" x2="12" y1="21" y2="12"></line>
              <line x1="12" x2="12" y1="8" y2="3"></line>
              <line x1="20" x2="20" y1="21" y2="16"></line>
              <line x1="20" x2="20" y1="12" y2="3"></line>
              <line x1="2" x2="6" y1="14" y2="14"></line>
              <line x1="10" x2="14" y1="8" y2="8"></line>
              <line x1="18" x2="22" y1="16" y2="16"></line>
            </svg>
            <p class="box-text-1">Hedge your positions</p>
            <p class="box-text-2">Go long and short at the same time on a specific instrument, with no interruption
              for traders using Expert Advisors (EAs).</p>

          </div>
          <div class="box">
            <svg xmlns="http://www.w3.org/2000/svg" width="65" height="65" viewBox="0 0 24 24" fill="none"
                 stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"
                 class="lucide lucide-banknote n-tile-icon n-tile-icon-icon">
              <rect width="20" height="12" x="2" y="6" rx="2"></rect>
              <circle cx="12" cy="12" r="2"></circle>
              <path d="M6 12h.01M18 12h.01"></path>
            </svg>
            <p class="box-text-1">Straightforward funding</p>
            <p class="box-text-2">Deposit and withdraw funds easily, and whenever you want to.</p>

          </div>
        </div>

      </div>

    </div>


  </div>
</template>

<script>
export default {
  name: "AboutSection8"
}
</script>

<style scoped>
.alpha{
  background-color: #000021;
  height: 100%;
  padding-top: 5%;
  padding-bottom: 5%;
}

.header{
  font-size: 30px;
  font-family: 'BR-Firma-Bold', sans-serif;
  color: #f7f7f7;
  text-align: center;
  padding-bottom: 4%;
}

.section-1{
  width: 50%;
  margin-left: 3%;
}

.section-2{
  width: 100%;
}

.section-2-inner{
  display: flex;
  justify-content: space-evenly;
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
  color: #f7f7f7;
  /*margin-bottom: 30px;*/
}
.button-group{
  display: flex;
  justify-content: left;
  gap: 10px;
}

.text-1{
  font-size: 34px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 40px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 8px;
  color: #f7f7f7;
}

.text-2{
  font-size: 17px;
  line-height: 23px;
  letter-spacing: -0.015em;
  text-align: left;
  color: #7A849D;
  margin-bottom: 24px;
}

.box {
  display: flex;
  flex-direction: column;
  border: 0.5px solid #dfdfdf;
  padding: 35px;
  border-radius: 10px;
  color: #f7f7f7;
  width: 600px;
  height: 280px;
  margin-bottom: 20px;
  margin-right: 20px;
}

.box-image{
  width: 10%;
}

.box-text-1{
  font-size: 26px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 30px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-top: 30px;
  margin-bottom: 20px;
  color: #f7f7f7;
}

.box-text-2{
  font-size: 15px;
  line-height: 25px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 20px;
  color: #7A849D;
}


.box-text-3{
  font-family: 'BR-Firma-Bold', sans-serif;
}

@media (max-width: 990px){

  .alpha{
    padding-top: 15%;
    padding-bottom: 15%;
  }

  .section-alpha{
    display: block;
  }

  .section-1{
    width: 100%;
    margin-left: unset;
  }

  .section-2{
    width: 100%;
  }

  .text-1{
    font-size: 30px;
    line-height: 30px;
    text-align: center;
  }

  .text-2{
    font-size: 15px;
    line-height: 20px;
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
    text-align: center;
  }

  .button-group{
    display: flex;
    justify-content: center;
    gap: 10px;
  }

  .section-2{
    margin-top: 10%;
  }
}

@media (max-width: 700px){
  .section-2-inner{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .box{
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
  }

  .box-text-1{
    font-size: 24px;
    line-height: 25px;
    margin-top: 15px;
    margin-bottom: 10px;
  }

  .box-text-2{
    font-size: 15px;
    line-height: 20px;
    margin-bottom: 15px;
  }

  .header{
    font-size: 27px;
    padding-bottom: unset;
  }
}
</style>
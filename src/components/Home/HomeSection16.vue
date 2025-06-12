<template>
  <div class="alpha">

    <div class="section-alpha">

      <div class="section-1">
        <div class="text-1">When they invest, <br/>
          you invest</div>

        <p class="text-2">You can use CopyTrader to copy the moves of other investors. Find users <br class="breaker" /> who match your
          investment plan and diversify with a click. <br class="breaker" /> You can use CopyTrader to copy the moves of other  investors.
          <br class="breaker" /> Find users who match your investment plan and diversify with a click.</p>


<!--        <div class="button-group">-->
<!--          <div class="btn-1" @click="onPostClick">-->
<!--            Start Trading-->
<!--          </div>-->
<!--          &lt;!&ndash;          <div class="btn-1" @click="onPostClick2">&ndash;&gt;-->
<!--          &lt;!&ndash;            LogIn&ndash;&gt;-->
<!--          &lt;!&ndash;          </div>&ndash;&gt;-->
<!--        </div>-->
      </div>

      <div class="section-2">
        <img src="@/assets/desktop_1.png" alt="" class="image" />
        <!--        <video autoplay="" muted="" loop="">-->
        <!--          <source src="https://margex.com/videos/header_mobile_video.mp4" type="video/mp4">-->
        <!--        </video>-->
      </div>

    </div>

    <div class="section-1">
      <p class="section-1-header">Show me the <span style="color: #1450C8">Most Copied</span> Over The Last <span style="color: #1450C8">Year</span></p>

      <div class="nav-btn">
        <i class='bx  bx-caret-left-circle' @click="onPostClick"  ></i>
        <i class='bx  bx-caret-right-circle'  @click="onPostClick2" ></i>
      </div>
    </div>

    <div v-show="this.screen === 'screen1' ">
      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>1</p>
            <img src="@/assets/thomas.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Thomas Parry Jones </p>
              <p style="color: #777;font-size: 14px">  @thomaspj </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  28,869  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>2</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/14959563/33.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Jay Smith  </p>
              <p style="color: #777;font-size: 14px"> @jaynemesis </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  10,305  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>3</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/2988943/7.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">Jeppe Kirk Bonde</p>
              <p style="color: #777;font-size: 14px">@JeppeKirkBonde</p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  29,903  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>4</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/5125148/5.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Zechariah Bin Zheng </p>
              <p style="color: #777;font-size: 14px">  @FundManagerZech </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">9,391</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>5</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/6216244/9.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Blue Screen Media ApS </p>
              <p style="color: #777;font-size: 14px"> @CPHequities </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  13,563  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>6</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/11132144/6.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Amit Kupfer </p>
              <p style="color: #777;font-size: 14px"> @AmitKup </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">8,725</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>7</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/18002171/4.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Pietari Laurila </p>
              <p style="color: #777;font-size: 14px"> @triangulacapital </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  12,608  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>8</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/11295345/10.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Greenbull Investments Sarl </p>
              <p style="color: #777;font-size: 14px"> @GreenbullInvest </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">6,983</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>9</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/5489903/6.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Heloise Greeff </p>
              <p style="color: #777;font-size: 14px"> @rubymza </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">6,132</p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>10</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/4356818/3.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Wesley Nolte </p>
              <p style="color: #777;font-size: 14px"> @Wesl3y </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">3,569</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>
    </div>

    <div v-show="this.screen === 'screen2' ">
      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>11</p>
            <img src="@/assets/thomas.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Stewart Fitzell </p>
              <p style="color: #777;font-size: 14px">  @defense_investor  </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  4,951  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>12</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/5970444/2.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Roberto Anzellotti </p>
              <p style="color: #777;font-size: 14px">  @IlMatematico </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  3,481  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>13</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/3568542/7.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> George Thomson </p>
              <p style="color: #777;font-size: 14px"> @misterg23 </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  3,977  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>14</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/3180395/2.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Mariano Daniel Pardo  </p>
              <p style="color: #777;font-size: 14px">  @MarianoPardo  </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">3,195</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>15</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/6253394/1.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Richard Stroud  </p>
              <p style="color: #777;font-size: 14px">  @Richardstroud </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  3,677  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>16</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/13335091/4.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Ingvar Rueckemann  </p>
              <p style="color: #777;font-size: 14px"> @ingruc </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">3,036</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>17</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/23325035/8.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Jorden Boer  </p>
              <p style="color: #777;font-size: 14px">  @JORDENBOER </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">  3,026  </p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>18</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/5970444/2.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Roberto Anzellotti </p>
              <p style="color: #777;font-size: 14px">  @IlMatematico </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">3,481</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>

      <div class="section-table">

        <div class="part-1">
          <div  class="part-1-inner">
            <p>19</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/14959563/33.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;">  Mike Moest  </p>
              <p style="color: #777;font-size: 14px">  @Aukie2008 </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">2,856</p>
            <p style="color: #777;font-size: 14px">  Copiers </p>
          </div>
        </div>

        <div class="part-2">
          <div  class="part-1-inner">
            <p>20</p>
            <img src="https://etoro-cdn.etorostatic.com/avatars/150X150/5166077/4.jpg" alt="" class="image-part-1" />
            <div class="part-1-inner-iii">
              <p style="color:#2c2c2c;"> Shao Feng Li </p>
              <p style="color: #777;font-size: 14px">  @steveli1029  </p>
            </div>
          </div>
          <div  class="part-2-inner">
            <p style="color: #1450C8">2,387</p>
            <p style="color: #777;font-size: 14px">Copiers</p>
          </div>
        </div>

      </div>
    </div>



  </div>
</template>

<script>
export default {
  name: "HomeSection16",
  data() {
    return {
      currentIndex: 0,
      items: [
        { name: 'Forex', color: '#009688' },  // Red
        { name: 'RealEstate', color: '#984613' }  ,  // Yellow
        { name: 'Crypto', color: '#3071EE' }, // Green
        { name: 'Stocks', color: '#5d78ff' }, // Blue
        { name: 'CFD', color: '#fe9431' }    // Yellow
      ],
      intervalId: null,
      screen: "screen1"
    };
  },
  mounted() {
    this.startRotation();
  },
  beforeDestroy() {
    clearInterval(this.intervalId);
  },
  methods: {
    startRotation() {
      this.intervalId = setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % this.items.length;
      }, 2000); // Change item every 2000 milliseconds
    },
    onPostClick() {
      this.screen = "screen1";
    },
    onPostClick2() {
      this.screen = "screen2";
    },
  }
}
</script>

<style scoped>
.alpha{
  margin-top: 1%;
  margin-bottom: 5%;
}
.section-alpha{
  height: 100%;
  display: flex;
  align-items: center;
  align-content: center;
  /* background-image: url("https://margex.com/images/bg_desk.webp");
   background-position: bottom;
   background-repeat: no-repeat;
   background-size: cover;
   position: relative;
  display: block;
  text-align: center;
  margin-left: auto;
  margin-right: auto;*/
}
.items-switch .active {
  display: inline; /* Show only active item */
}
.items-switch .active {
  display: inline; /* Show only active item */
}

.items-switch span {
  display: none; /* Hide all by default */
}

.section-1{
  width: 50%;
  margin-left: 5%;
}

.section-2{
  width: 50%;
  margin-right: 1%;
  /*margin-bottom: -10px;
  width: 255px;
  height: 500px;
  background: url("https://margex.com/images/phone_border.svg");
  background-repeat: no-repeat;
  -webkit-background-position: center;
  background-position: center;
  -webkit-background-size: contain;
  background-size: contain;
  padding: 12px 16px 0;
  margin-top: 2%;
  display: block;
  margin-left: auto;
  margin-right: auto;*/
}

video{
  width: 100%;
  border-radius: 30px;
}
.text-1{
  font-size: 40px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 40px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 8px;
  color: #000021;
}

.text-2{
  font-size: 17px;
  line-height: 25px;
  letter-spacing: -0.015em;
  text-align: left;
  color: #7A849D;
  margin-bottom: 24px;
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
  width: 180px;
  /*margin-left: auto;*/
  /*margin-right: auto;*/
  color: #FFFFFF;
  /*margin-bottom: 30px;*/
}

.image{
  width: 100%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.section-1-header{
  font-size: 22px;
  font-weight: 900;
}

.section-1 {
  margin-top: 1%;
  margin-bottom: 1%;
  width: 85%;
}

.nav-btn{
  display: flex;
  justify-content: right;
  gap: 5px;
  margin-top: 1%;
}

.bx-caret-left-circle{
  font-size: 32px;
  color: #cfcfcf;
}

.bx-caret-left-circle:hover{
  color: #1450C8;
}

.bx-caret-right-circle{
  font-size: 32px;
  color: #cfcfcf;
}

.bx-caret-right-circle:hover{
  color: #1450C8;
}

.section-table{
  display: flex;
  margin-bottom: 30px;
}

.part-1{
  width: 50%;
  display: flex;
  justify-content: space-between;
  margin-right: 2%;
  margin-left: 5%;
  border-bottom: 1px solid #f1f1f1;
}

.part-2 {
  width: 50%;
  display: flex;
  justify-content: space-between;
  margin-right: 5%;
  margin-left: 2%;
  border-bottom: 1px solid #f1f1f1;
}

.part-1-inner{
  display: flex;
  gap: 8px;
}

.image-part-1{
  width: 15%;
  margin-bottom: 1.5%;
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {

  .section-alpha{
    height: 100%;
    padding-top: 5%;
    padding-bottom: 5%;
  }

  .section-alpha{
    display: block;
  }

  .section-1{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .text-1{
    font-size: 43px;
    line-height: 45px;
    margin-bottom: 8px;
    text-align: center;
  }

  .text-2{
    font-size: 15px;
    line-height: 22px;
    text-align: center;
  }

  .btn-1{
    height: 40px;
    padding: 8px 16px;
    gap: 6px;
    width: 160px;
    font-size: 14px;
  }

  .button-group{
    display: flex;
    justify-content: center;
    gap: 12px;
  }

  .section-2{
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 5%;
    width: 100%;
  }

  .section-1{
    width: 100%;
  }

  video{
    width: 100%;
    border-radius: 30px;
  }

  .image{
    width: 85%;
  }

  .section-table{
    display: block;
  }

  .part-1{
    width: 90%;
    margin-right: auto;
    margin-left: auto;
    margin-bottom: 20px;
  }

  .part-2 {
    width: 90%;
    margin-right: auto;
    margin-left: auto;
  }

  .section-1-header{
    margin-left: 3%;
  }

  .nav-btn{
    margin-top: 2%;
    margin-bottom: 1%;
  }

  .breaker{
    display: none;
  }
}

@media (max-width: 500px) {
  .text-1{
    font-size: 30px;
    line-height: 35px;
    margin-bottom: 9px;
  }

  .text-2{
    width: 85%;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
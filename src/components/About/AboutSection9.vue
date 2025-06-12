<template>
  <div class="alpha">

    <div class="section-alpha">

      <div class="section-1">
        <p class="text-1">Superior execution and reliability</p>
        <p class="text-2">Our pioneering technology and highly-regarded customer service, alongside a choice of
          powerful platforms, offers an ideal combination for serious traders.</p>

        <div class="button-group">
          <div class="btn-1" @click="onPostClick">
            Open Account
          </div>
          <div class="btn-1" @click="onPostClick2">
            LogIn
          </div>
        </div>
      </div>

      <div class="section-2">

        <div class="section-2-inner">
          <div class="box">
            <img src="https://images.ctfassets.net/vl2kvsmutclx/68sWV1PdMHabdENyNA2SXA/2face6889ee29199ff57dbcecfe78ba3/100perc.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">Automated execution</p>
            <p class="box-text-2">Your trades will be filled without any dealer intervention.</p>
          </div>
        </div>

        <div class="section-2-inner">
          <div class="box">
            <img src="https://images.ctfassets.net/vl2kvsmutclx/2wdzg6u7zGQldJnuf1nawl/c48303e58e9d163a723a0d15c094a964/97.9-__2_.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">Fill rate</p>
            <p class="box-text-2">We fulfil your order without off-quotes, and wherever possible at the price you see.</p>

          </div>
        </div>

        <div class="section-2-inner">
          <div class="box">
            <img src="https://images.ctfassets.net/vl2kvsmutclx/4bIjdaH73as2VSkn4vJun0/fa3d9e24392b6717a84aaea18cecab28/99.99-_.svg" alt="icon" class="box-image"/>
            <p class="box-text-1">Platform stability</p>
            <p class="box-text-2">We consistently achieve almost 100% core platform uptime, so you can focus on your trading.</p>


          </div>
        </div>

      </div>

    </div>


  </div>
</template>

<script>
export default {
  name: "AboutSection9",
  methods: {
    onPostClick() {
      this.$router.push("/register");
    },
    onPostClick2() {
      this.$router.push("/login");
    },
  }
}
</script>

<style scoped>
.alpha{
  background-color: #000021;
  height: 100%;
  padding-top: 10%;
  padding-bottom: 5%;
}

.section-alpha{
  display: flex;
}

.section-1{
  width: 50%;
  margin-left: 3%;
}

.section-2{
  width: 50%;
}

.section-2-inner{
  display: flex;
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
  display: block;
  border: 0.5px solid #dfdfdf;
  padding: 20px;
  border-radius: 10px;
  color: #fff;
  width: 90%;
  height: 100%;
  margin-bottom: 20px;
  margin-right: auto;
  margin-left: auto;
}

.box-image{
  width: 20%;
}

.box-text-1{
  font-size: 27px;
  font-family: 'BR-Firma-Bold', sans-serif;
  line-height: 30px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-top: 30px;
  margin-bottom: 10px;
  color: #f7f7f7;
}

.box-text-2{
  font-size: 15px;
  line-height: 25px;
  letter-spacing: -0.01em;
  text-align: left;
  margin-bottom: 30px;
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
  }

  .box-text-1{
    margin-top: 20px;
  }

  .box-image{
    margin-top: 5%;
  }
}
</style>
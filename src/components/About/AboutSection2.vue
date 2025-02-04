<template>
  <div class="alpha">
    <p class="section-header-1">There’s a time and a place for risk</p>
    <p class="section-header">Your funds and data are always secure. With Early Wealth you’re protected
      by industry-leading protocols.</p>


    <div class="section-alpha">

      <div class="section-1">

        <div class="text-part">
          <p class="text-1">Setting New Standards in Global Finance Technology</p>
          <p class="text-2">Early Wealth is set on a mission to provide a fair, secure, and easy-to-use
            platform with the highest class of financial technologies globally.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Simplifying Complex Systems for Everyone</p>
          <p class="text-2">
            We strongly believe that everyone should be able to enjoy equal and unrestricted wealth-building
            opportunities no matter who you are and where you live. Our goal is to make complex systems simple to
            understand and easy to use.
          </p>
          <br/>
          <p class="text-1">Multiple regulatory licenses</p>
          <p class="text-2">We are licensed and regulated by leading international governing bodies. Trade knowing
            your financial data is protected.</p>
        </div>



      </div>

      <div class="section-2">

        <img src="https://margex.com/_next/image?url=%2Fimages%2Fabout_belief.png&w=1920&q=75" alt="image" class="image" />

      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection2"
}
</script>

<style scoped>
/*.alpha{*/
/*  !*background-color: #f0f2f4;*!*/
/*  padding-bottom: 3%;*/
/*  padding-top: 3%;*/
/*}*/
.alpha{
  padding-top: 5%;
  padding-bottom: 5%;
  background: #f4f5f6;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
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
.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  margin-top: 3%;
}

.image{
  width: 100%;
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
  line-height: 24px;
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
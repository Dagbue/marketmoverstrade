<template>
  <div class="alpha">

    <div class="section-1">
      <h2 class="text-1" style="text-align: center;">Powerful web and mobile trading platforms.</h2>
      <p class="text-2" style="text-align: center;">All-Inclusive suite for investing, brokerage,
        custody and post-trade processing.</p>
      <img src="https://assets.cmcmarkets.com/images/platform_device_cluster_group_extra.png" alt="" class="image"/>
      <div class="section-1-inner">


        <div class="section-1-inner-content">
          <i class='bx bx-tab'></i>
          <p>Tablet</p>
        </div>

        <div class="section-1-inner-content">
          <i class='bx bx-mobile'></i>
          <p>Phone</p>
        </div>

        <div class="section-1-inner-content">
          <i class='bx bx-laptop' ></i>
          <p>Laptop</p>
        </div>


      </div>

      <p class="text-2" style="text-align: center;">Coming Soon On</p>

      <div class="image-part">
        <img src="https://assets.cmcmarkets.com/images/apple-app-store_extra.webp" alt="" class="image2" />

        <img src="https://assets.cmcmarkets.com/images/google-play_extra.jpg" alt="" class="image2" />
      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection9",
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
  background: #f4f5f6;
}
.section-1-inner{
  display: flex;
  justify-content: center;
  gap: 20px;
}
.section-1-inner-content{
  text-align: center;
}
.section-1-inner-content p{
  font-size: 17px;
}
.image{
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.text-1{
  font-size: 25px;
  font-family: 'BR-Firma-Bold', sans-serif;
  padding-bottom: 5px;
}
.text-2{
  font-size: 18px;
  text-align: center;
  padding-bottom: 2.5%;
}
.bx{
  font-size: 30px;
  margin-top: 10px;
}

.image-part{
  display: flex;
  justify-content: center;
  gap: 20px;
}



@media (max-width: 990px){

  .image{
    width: 100%;
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-top: 3%;
  }


  .image2{
    width: 25%;
  }


}

@media (max-width: 500px){

}
</style>
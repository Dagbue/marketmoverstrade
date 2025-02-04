<template>
  <div>
    <hero-section/>
    <retirement-planning/>
    <home-section2/>
    <home-section1/>
    <home-section4/>
    <home-section5/>
    <features-part/>
    <get-started/>
    <home-section7/>
    <home-section8/>
    <blog-table/>
    <home-section9/>
    <ready-to-work/>
    <footer-home/>
  </div>
</template>

<script>
// @ is an alias to /src

import HeroSection from "@/components/Home/HeroSection.vue";
import HomeSection1 from "@/components/Home/HomeSection1.vue";
import HomeSection2 from "@/components/Home/HomeSection2.vue";
import HomeSection4 from "@/components/Home/HomeSection4.vue";
import HomeSection5 from "@/components/Home/HomeSection5.vue";
import FeaturesPart from "@/components/Home/FeaturesPart.vue";
import GetStarted from "@/components/Home/GetStarted.vue";
import HomeSection7 from "@/components/Home/HomeSection7.vue";
import HomeSection8 from "@/components/Home/HomeSection8.vue";
import HomeSection9 from "@/components/Home/HomeSection9.vue";
import ReadyToWork from "@/components/Home/ReadyToWork.vue";
import FooterHome from "@/components/BaseComponents/FooterHome.vue";
import BlogTable from "@/components/BaseComponents/tables/BlogTable.vue";
import RetirementPlanning from "@/components/Home/RetirementPlanning.vue";

export default {
  name: 'HomeView',
  components: {
    RetirementPlanning,
    BlogTable,
    FooterHome,
    ReadyToWork,
    HomeSection9,
    HomeSection8,
    HomeSection7,
    GetStarted, FeaturesPart, HomeSection5, HomeSection4, HomeSection2, HomeSection1, HeroSection},
}
</script>

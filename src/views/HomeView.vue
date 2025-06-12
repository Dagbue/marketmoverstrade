<template>
  <div>
    <hero-section/>
    <home-section11/>
    <home-section12/>
    <home-section13/>
    <home-section14/>
    <home-section16/>
    <home-section8/>
    <blog-table/>
    <home-section7/>
    <ready-to-work/>
    <footer-home/>
  </div>
</template>

<script>
// @ is an alias to /src

import HeroSection from "@/components/Home/HeroSection.vue";
import ReadyToWork from "@/components/Home/ReadyToWork.vue";
import FooterHome from "@/components/BaseComponents/FooterHome.vue";
import HomeSection11 from "@/components/Home/HomeSection11.vue";
import HomeSection12 from "@/components/Home/HomeSection12.vue";
import HomeSection13 from "@/components/Home/HomeSection13.vue";
import HomeSection14 from "@/components/Home/HomeSection14.vue";
import HomeSection8 from "@/components/Home/HomeSection8.vue";
import BlogTable from "@/components/BaseComponents/tables/BlogTable.vue";
import HomeSection7 from "@/components/Home/HomeSection7.vue";
import HomeSection16 from "@/components/Home/HomeSection16.vue";

export default {
  name: 'HomeView',
  components: {
    HomeSection16,
    HomeSection7,
    BlogTable,
    HomeSection8,
    HomeSection14,
    HomeSection13,
    HomeSection12,
    HomeSection11,
    FooterHome,
    ReadyToWork,
    HeroSection
  },
}
</script>

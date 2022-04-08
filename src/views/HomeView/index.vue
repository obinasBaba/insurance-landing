<template>
  <div class="home">

    <HeroView/>
    <ServiceView/>
    <AboutView/>
    <ContactView/>
    <FooterView/>

  </div>
</template>

<script>

import HeroView from "@/views/HomeView/Sections/HeroView";
import AboutView from "@/views/HomeView/Sections/AboutView";
import ContactView from "@/views/HomeView/Sections/ContactView";
import ServiceView from "@/views/HomeView/Sections/ServiceView";
import FooterView from "@/views/HomeView/Sections/FooterView";

export default {
  name: "HomeView",
  components: { FooterView, ServiceView, ContactView, AboutView, HeroView },
  setup(){

  },
};
</script>

<style lang="scss" scoped>
@use '~@/styles' as s;


.home {
  position: relative;
  height: 100%;
  width: 100%;
  margin: 0 auto;

  //background:radial-gradient(ellipse at bottom, rgba(255,254,234,1) 0%, rgba(255,254,234,1) 35%, #B7E8EB 100%);
  overflow: hidden;

  background-color: s.$clrs-main-bg;


}


</style>
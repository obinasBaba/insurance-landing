<template>
  <div class="home">

    <HeroView/>
    <AboutView/>
    <ContactView/>

  </div>
</template>

<script>

import HeroView from "@/views/HomeView/Sections/HeroView";
import AboutView from "@/views/HomeView/Sections/AboutView";
import ContactView from "@/views/HomeView/Sections/ContactView";

export default {
  name: "HomeView",
  components: { ContactView, AboutView, HeroView },
  setup(){

  },
};
</script>

<style lang="scss" scoped>

.home {
  position: relative;
  height: 100%;
  width: 100%;
  margin: 0 auto;

  //background:radial-gradient(ellipse at bottom, rgba(255,254,234,1) 0%, rgba(255,254,234,1) 35%, #B7E8EB 100%);
  overflow: hidden;


}


</style>
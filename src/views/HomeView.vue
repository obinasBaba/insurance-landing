<template>
  <div class="home">
    <FancyButton/>
    <h1>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet dignissimos esse exercitationem hic id molestias
      officiis pariatur praesentium, sed voluptatum.
    </h1>
  </div>
</template>

<script>
// @ is an alias to /src
import FancyButton from "@/components/FancyButton";

export default {
  name: "HomeView",
  components: {
    FancyButton,
  },
};
</script>

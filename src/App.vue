<template>
  <div class="app-container">
    <AppNavBar/>
    <router-view/>
  </div>
</template>

<script>
import AppNavBar from "@/components/AppNavBar";

export default {
  components: { AppNavBar }
}
</script>

<style lang="scss">
@use "styles/global-style";

#app {

  .app-container {

  }

}

</style>

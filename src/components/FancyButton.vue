<template>
  <button class="fancy-btn">get quote now</button>
</template>

<script>
export default {
  name: "FancyButton",
};
</script>

<style scoped lang="scss">
@use "~@/styles" as styl;

.fancy-btn {
  border-radius: 5000px;
  background-color: styl.$clrs-accent;
  border: none;
  font-family: styl.$fonts-auger;
  text-transform: capitalize;

  font-weight: bold;
  color: darken(#29C1FF, 30%);



  @include styl.padding(hor, 1rem);
  @include styl.padding(ver, .5rem);
}
</style>

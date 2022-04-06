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
  color: white;
  font-family: styl.$fonts-auger;
  text-transform: capitalize;

  @include styl.padding(hor, 2rem);
  @include styl.padding(ver, 1rem);
}
</style>

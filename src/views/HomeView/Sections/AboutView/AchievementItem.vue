<template>
  <div class="achievement">
    <div class="icon">
      <img :src="achievement.src" alt="ac">
    </div>
    <p>{{ achievement.text[0] }} <br/> {{achievement.text[1]}} </p>
  </div>
</template>

<script>
export default {
  name: "AchievementItem",
  props: {
    achievement: Object,
  }
}
</script>

<style scoped lang="scss">
@use '~@/styles' as s;


.achievement{
  display: flex;
  align-items: center;
  gap: 1vmax;
  margin-top: 3vmax;

  .icon{
    display: grid;
    place-items: center;
    width: 50px;
    height: 50px;
    border-radius: 50%;

    background-color: s.$clrs-main-color;
  }

  p{
    color: s.$clrs-main-color;
    font-family: s.$fonts-auger-900;
    letter-spacing: .5px;
  }
}

</style>
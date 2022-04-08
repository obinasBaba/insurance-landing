<template>
  <div class="about-view">


    <div class="about-txt-container">
      <div class="txt-large">
        <p><strong>The Best Choice</strong></p>
        <h1>About Us</h1>
      </div>

      <div class="about-txt">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. A deserunt est exercitationem fugiat laboriosam
          mollitia, <strong>natus nostrum obcaecati officia </strong> quo quod rem sed soluta ut voluptatem? Dolorem itaque numquam
          praesentium.
        </p>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur exsam magnam modi odit
          quibusdam quidem <strong> ratione temporibus voluptate</strong>.
        </p>
      </div>
    </div>


    <div class="achievements">
      <AchievementItem v-for="achievement in achievements" :achievement="achievement" :key="achievement"/>
    </div>

  </div>
</template>

<script>
import AchievementItem from "@/views/HomeView/Sections/AboutView/AchievementItem";

export default {
  name: "AboutView",
  components: { AchievementItem },
  setup(){
    const achievements = [{
      src: '',
      text: ['Best Price ', 'on the market'],
    }, {
      src: '',
      text: ['The largest choice', '  of insurance'],
    }, {
      src: '',
      text: ['Individual ', ' approach'],
    }, {
      src: '',
      text:[ '15 years of ', ' experience'],
    }];

    return {
      achievements,
    }
  }
}
</script>

<style scoped lang="scss">
@use '~@/styles' as s;

.about-view {
  max-width: 1400px;
  margin: 10vmax auto 0;
  color: black;


  .about-txt-container{
    display: flex;
    justify-content: center;
    //gap: s.fluid-unit(5rem);
    @include s.fluid-props(gap, 5rem);


    .txt-large{
      & *{
        word-break: keep-all;
      }

      strong{
        color: lighten(#29C1FF, 10%);
        font-weight: bolder;
        //margin-bottom: 0;
      }

      h1{
        @include s.font-size-title(3.5rem);
        font-family: s.$fonts-auger-900;
        word-spacing: -1vmax;

      }
    }

    .about-txt{
      max-width: 50%;
      color: lighten(grey, 10%);
      @include s.font-size-text(.9rem);
    }
  }

  .achievements{
    display: flex;
    justify-content: space-evenly;
    //gap: 3rem;
  }

}


</style>
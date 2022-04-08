<template>
  <div class="hero-view">

    <div class="content">

      <div class="txt-container">
        <p><strong>Be Smart</strong></p>
        <h1 class="large" >Get Best <br> Insurance Deals</h1>
        <p class="desc">Best Insurance helps you get the <strong>best <br> insurance</strong> quote <strong>fast and easily!</strong> </p>
      </div>

      <div class="img-container">
        <img src="/hero-image.png">
      </div>

    </div>

    <div class="bg">
      <div class="wave" style="background-image: url('./wave.svg')" ></div>
    </div>

  </div>
</template>

<script>
export default {
  name: "HomeView"
}
</script>

<style scoped lang="scss" >
@use "~@/styles" as styl;

.hero-view{
  position: relative;
  min-height: 80vh;

  .content{
    position: relative;
    display: flex;
    justify-content: space-evenly;
    max-width: 1400px;
    z-index: 1;
    //border: thin solid red;
    margin: 0 auto;

    .txt-container{
      display: flex;
      flex-flow: column;
      align-items: flex-start;
      margin-top: 12vmax;

      h1.large{
        font-family: styl.$fonts-auger-900;
        @include styl.font-size-title(3.5rem);
        font-weight: bolder;
        letter-spacing: 0;
        word-spacing: -1vmax;
        line-height: .9;
      }

      p{
        color: lighten(#29C1FF, 20%);
        @include styl.font-size-text(.9rem);

        strong{
          color: lighten(#29C1FF, 30%);
          font-weight: bolder;
        }
      }
    }

    .img-container{
      //align-self: flex-end;
      margin-top: 10vmax;
    }

  }



  .bg {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 0;
    height: 75%;
    width: 100%;
    background: styl.$clrs-main-color;

    .wave {
      background-repeat: repeat-x;
      position: absolute;
      bottom: -168px;
      width: 6400px;
      height: 198px;
      animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite, swell 7s ease -1.25s infinite;
      transform: translate3d(0, 0, 0) rotate(180deg);
    }

    .wave:nth-of-type(2) {
      bottom: -175px;
      animation: wave 7s cubic-bezier( 0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
      opacity: 1;
    }

    @keyframes swell {
      0%, 100% {
        transform: translate3d(0, -45px, 0) rotate(180deg);
      }

      50% {
        transform: translate3d(0, 28px, 0) rotate(180deg);
      }
    }

    @keyframes wave {
      0% {
        margin-left: 0;
      }
      100% {
        margin-left: -1600px;
      }
    }

  }
}



</style>
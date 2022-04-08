<template>
  <div class="contact-view">
    <div class="content">
      <div class="title">
        <p><strong>Don't wait</strong></p>
        <h1>Contact Us</h1>
      </div>
      <div class="contact-txt">
        <p class="intro">Should you have any questions, or wish to speak to one of our Qualified Financial Adviser at Oaktree finance
          service, Please contact us</p>

        <div class="address-txt">
          <div class="address">
            <div>
              <h4 class="title">Oaktree finance service LTD.,</h4>
              <p>20 Kent Street, Fermoy, Co, Cork</p>
              <p>Phone: 025 50886</p>
            </div>

            <div>
              <p>Locall: 1879 74433434</p>
              <p>Fax: 2929 240218</p>
              <p class="email">Email: <strong>info@oaktreefinance.et</strong></p>
            </div>
          </div>

          <div class="address">
            <div>
              <h4 class="title">Oaktree finance service LTD.,</h4>
              <p>1021Lake Drive, CityWest Business Campus</p>
              <p>Addis 24 phone: 923 3636 5539</p>
            </div>

            <div class="btn">
              <FancyButton/>
            </div>

          </div>
        </div>

      </div>
    </div>

    <div class="world-map">
      <img src="/world-map.png" alt="world-map">
    </div>

    <div class="contact-wave">
      <div class="wave" style="background-image: url('/contact-wave.svg')"></div>
    </div>

  </div>
</template>

<script>
import FancyButton from "@/components/FancyButton";

export default {
  name: "ContactView",
  components: { FancyButton }
}
</script>

<style scoped lang="scss">
@use '~@/styles' as s;

.contact-view {
  position: relative;
  width: 100%;
  background-color: s.$clrs-contact-bg;
  display: flex;
  margin-top: 20vmax;


  .content {
    display: flex;
    justify-content: space-evenly;
    //border: thin solid red;
    max-width: 1400px;
    margin: 13vmax auto;
    color: black;

    .intro{
      @include s.font-size-text(1rem);
      color: darken(grey, 9%);
    }


    .title {
      position: relative;

      p {
        strong {
          color: lighten(#29C1FF, 10%);
          font-weight: bolder;
          position: absolute;
          top: -.3vmax;
        }
      }

      h1 {
        @include s.font-size-title(3.5rem);
        font-family: s.$fonts-auger-900;
        word-spacing: -1vmax;
      }
    }

    .contact-txt {
      //border: thin solid red;
      max-width: 54%;
      color: lighten(grey, 10%);

      .address-txt {
        margin-top: 4.5vmax;
        display: flex;
        justify-content: space-between;
        //gap: s.fluid-unit(rem);


        .address {
          display: flex;
          flex-flow: column;
          gap: s.fluid-unit(1.5rem);

          .title {
            color: black;
            font-weight: bold;
            font-family: s.$fonts-auger-500;
          }

          & .btn {
            margin-top: auto;
            margin-bottom: auto;
          }

          & .email {
            strong {
              color: lighten(#29C1FF, 10%);
              text-decoration: underline;
              opacity: .6;
            }
          }

          & * {
            //font-size: initial;
            margin: 0;
          }

          & p {
            word-spacing: -.2vmax;
          }
        }
      }
    }
  }

  .world-map {
    position: absolute;
    display: grid;
    place-items: center;
    z-index: 1;

    img {
      max-width: 80%;
      opacity: .2;
      margin-left: 4vmax;
    }
  }

  .contact-wave {
    position: absolute;
    top: 0;
    left: 0;
    height: 0px;
    width: 100%;
    background: s.$clrs-contact-bg;
    //z-index: -1;

    .wave {
      background-repeat: repeat-x;
      position: absolute;
      //bottom: -168px;
      top: -168px;

      width: 6400px;
      height: 198px;
      animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite, swell 7s ease -1.25s infinite;
      transform: translate3d(0, 0, 0);

      @keyframes wave {
        0% {
          margin-left: 0;
        }
        100% {
          margin-left: -1600px;
        }
      }

      @keyframes swell {
        0%, 100% {
          transform: translate3d(0, -25px, 0);
        }

        50% {
          transform: translate3d(0, 28px, 0);
        }
      }
    }
  }

}

</style>
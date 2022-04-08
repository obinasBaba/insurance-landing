<template>
  <footer class="footer">

    <div class="content">
      <div class="terms">
        <div class="logo-term">
          <img src="/app-logo.png" alt="app-logo">
          <p><strong >Terms Of Business</strong></p>
        </div>

        <p class="copyright">
          &copy; Copyright 2022 by <strong>bestinsure.et</strong> All right reserved<br/>
          This material may not be duplicated for any profit-driven enterprise.
        </p>
      </div>

      <div class="call">
        <div class="phone">
          <img src="/phone-icon.png" alt="phone-icon">
         <h3> 1890 856 023</h3>
        </div>

        <p> <strong>bestinsure.et</strong> is regulated by the Central Bank of Ireland </p>
      </div>

      <div class="sign">
        <p>created by </p> 
        <img src="/signature.png" alt="signature">
      </div>

    </div>

    <div class="footer-wave">
      <div class="wave" style="background-image: url('/wave.svg')"></div>
    </div>


  </footer>
</template>

<script>
export default {
  name: "FooterView"
}
</script>

<style scoped lang="scss" >
@use '~@/styles' as s;

.footer{
  position: relative;
  border: thin solid gold;
  background-color: s.$clrs-main-color;

  .content {
    position: relative;
    z-index: 5;
    display: flex;
    justify-content: space-evenly;
    padding-bottom: 1rem;
    margin: 0 auto;
    max-width: 1550px;



    .terms{
      .logo-term{
        display: flex;
        align-items: center;
        gap: s.fluid-unit(1rem);
      }

      strong{
        color: lighten(#29C1FF, 30%);
        font-weight: bolder;
        text-decoration: underline;
        margin: 0;
      }

      .copyright{
        word-spacing: -.2vmax;
      }
    }

    .call{
      display: flex;
      flex-flow: column;
      justify-content: space-evenly;

      .phone{
        display: flex;
        align-items: center;
        gap: s.fluid-unit(1rem);
        margin-top: auto;
      }
      p{
        //margin-top: auto;
        word-spacing: -.2vmax;

      }
    }

    .sign{
      display: flex;
      align-items: center;
      gap: s.fluid-unit(.5rem);
      margin-top: auto;

    }
  }

  .footer-wave {
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
          transform: translate3d(0, -15px, 0);
        }

        50% {
          transform: translate3d(0, 18px, 0);
        }
      }
    }
  }


}

</style>
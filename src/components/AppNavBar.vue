<template>
  <nav>
    <div class="logo">
      <img src="/app-logo.png" alt="logo">
    </div>

    <div class="links">
      <a href="#home"> Home </a>
      <a href="#about"> About Us </a>
      <a href="#contact"> Contact Us </a>
    </div>

    <div class="contact">
      <div class="phone">
        <img src="/phone-icon.png" alt="phone-icon">
        <span>1890 856 023</span>
      </div>
      <FancyButton text="Get Quote Now"/>
    </div>

  </nav>
</template>

<script>
import FancyButton from "@/components/FancyButton";

export default {
  name: "AppNavBar",
  components: { FancyButton }
}
</script>

<style scoped lang="scss">
@use '~@/styles' as s;

nav {
  position: fixed;
  z-index: 10;
  top: 1vmax;
  left: 0;
  right: 0;

  max-width: 1500px;
  width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;


  .logo{

  }

  .links{
    display: flex;
    gap: 2rem;

    a{
      color: lighten(#29C1FF, 30%);
      font-family: s.$fonts-auger-500;
      text-decoration: none;
      @include s.font-size-text(.9rem);
      letter-spacing: .3px;
    }
  }

  .contact{
    display: flex;
    align-items: center;
    gap: 1.5rem;

    .phone{
      display: flex;
      align-items: center;
      gap: .5rem;

      img{
      }
    }
  }
}

</style>
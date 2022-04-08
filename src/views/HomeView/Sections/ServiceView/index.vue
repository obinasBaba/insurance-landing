<template>
  <div class="service">
    <div class="content">
      <ServiceItem  v-for="(service, idx) in services" :key="service" :content="services" :idx="idx" />
    </div>

    <div class="best-circle-rotation"  >
      <img src="/best-price-circle.png" alt="circle">
    </div>

  </div>
</template>

<script>
import ServiceItem from "@/views/HomeView/Sections/ServiceView/components/ServiceItem";
export default {
  name: "ServiceView",
  components: { ServiceItem },
  setup(){

    const services = [ {}, {}, {}, {}, {}, {}, {}, {} ];

    return {
      services,
    }
  }
}
</script>

<style scoped lang="scss" >
.service{
  position: relative;
  max-width: 1200px;
  margin: 4vmax auto 0;

  .content{
    display: grid;
    place-content: center;
    grid-template-columns: repeat(auto-fill, 250px);

    column-gap: 2.5rem;
    row-gap: 3rem;
  }

  .best-circle-rotation{
    position: absolute;
    bottom: -50px;
    right: -10%;

    img{
      animation: rotate 8s linear  forwards infinite;
      max-width: 200px;


      @keyframes rotate {
        0%{
          transform: rotate(0);
        }
        100%{
          transform: rotate(360deg);
        }
      }
    }
  }

}

</style>
<template>
  <div class="box" :style="style" >

  </div>
</template>

<script>
export default {
  name: "ServiceItem",
  props: {
    content: Object,
    idx: Number,
  },
  setup(props){
    const margin = props.idx < 4 ? `-${props.idx * 4.5}rem` : `-${(props.idx - 4) * 4.5 }rem`;
    return {
      style: {
        marginTop: margin,
      }
    }
  },
}
</script>

<style scoped lang="scss" >

.box{
  background: whitesmoke;
  box-shadow: 0 4px 21px 6px rgba(0, 0, 0, 0.13);

  //align-self: stretch;
  //width: 100%;
  //max-width: calc(100% / 5);
  border-radius: 20px;

  height: 200px;
}

</style>
<template>
  <Warm></Warm>
</template>

<script>
import Warm from "@/components/weather/Warm.vue";

export default {
  name: "Weather",
  components: {
    Warm
  },
  created(){
    this.$emit('showBar');
    console.log(this.showBar);
    this.showBar = false;
  }
};
</script>
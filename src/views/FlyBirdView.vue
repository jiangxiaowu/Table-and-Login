<template>
  <Flybird />
</template>

<script>
import Flybird from "@/components/bird/Flybird.vue";

export default {
  name: "Bird",
  components: {
    Flybird,
  },
  mounted() {
    console.log("flybird view");
  },
};
</script>
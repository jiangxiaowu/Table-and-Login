<template>
  <Player />
</template>

<script>
import Player from "@/components/music/Player.vue";

export default {
  name: "Music",
  components: {
    Player,
  },
  mounted() {
    console.log("music");
  },
};
</script>
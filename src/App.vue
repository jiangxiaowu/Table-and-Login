<template>
  <v-app>
    <PToolbar v-if="reloadHeader()" />

    <v-main style="background-color: white">
      <router-view />
    </v-main>

    <PFooter />
  </v-app>
</template>

<script>
import PToolbar from "./components//homepage/PToolbar";
import PFooter from "./components/homepage/PFooter";

export default {
  name: "App",
  components: {
    PToolbar,
    PFooter,
  },
  data: () => ({
    headerDisplay: true,
  }),
  methods: {
    reloadHeader() {
      console.log(this.$route.params.display);
      if(this.$route.params.display === undefined){
        return true;
      }
      return this.$route.params.display;
    },
  },
  // mounted() {
  //   this.reloadHeader(true);
  // },
};
</script>



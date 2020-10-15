<template>
  <v-app>
    <PToolbar />
    <v-content style="background-color: white">
      <router-view />
    </v-content>
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
    PFooter
  },

  data: () => ({
    //
  })
};
</script>

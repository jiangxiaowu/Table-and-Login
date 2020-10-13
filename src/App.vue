<template>
  <v-app>
    <!-- <router-link to="/">Home</router-link>
    <router-link to="/about">Page</router-link> -->
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
// import Navbar from "./components/Navbar";
export default {
  name: "App",

  components: {
    // Navbar,
  },

  data: () => ({
    //
  }),
};
</script>

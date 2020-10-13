<template>
  <v-app>
    <v-content>
      <!-- <router-link to="/login">Login</router-link> -->
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {
 
  },

  data: () => ({
    //
  }),
};
</script>

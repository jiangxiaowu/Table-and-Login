<template>
  <v-app-bar flat relatively height="60px" id="home">
    <v-layout justify-center>
      <v-container>
        <v-layout>
          <v-tab
            :class="{
              'display-1 font-weight-bold': $vuetify.breakpoint.smAndUp,
              'title font-weight-bold': $vuetify.breakpoint.smAndDown,
            }"
            to="/"
            
          >
            The Ville
          </v-tab>
          <v-spacer></v-spacer>
          <v-toolbar-items class="text-right">
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#about', options)"
              text
              >About</v-btn
            >
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#portfolio', options)"
              text
              >My Work</v-btn
            >
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#contact', options)"
              text
              >Contact</v-btn
            >
            <v-btn :x-small="$vuetify.breakpoint.smAndDown" @click="jump" text
              >Login</v-btn
            >
          </v-toolbar-items>
        </v-layout>
      </v-container>
    </v-layout>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic",
      },
    };
  },
  methods: {
    jump() {
      this.$router.push({ name: "Login", params: { display: true } });
    },
  },
  mounted() {},
};
</script>

<style>
</style>
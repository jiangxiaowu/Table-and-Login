<template>
  <v-card flat color="transparent" max-width="350px">
    <v-card-title>
      <v-layout>
        <v-flex xs7>
          <div>{{ app.name }}</div>
          <div>
            <v-chip small pill color="blue" dark>{{ app.price }}</v-chip>
          </div>

          <template v-for="(platform, i) in app.platforms">
            <v-btn :href="platform.link" target="_blank" icon :key="i">
              <v-icon>{{ platform.icon }}</v-icon>
            </v-btn>
          </template>
        </v-flex>
        <v-flex>
          <v-btn small @click="topath(app.path)">Click me</v-btn>
        </v-flex>
      </v-layout>
    </v-card-title>
    <v-card-text>
      <div>{{ app.description }}</div>
      <div class="title mt-2">Technologies Used</div>
      <v-layout>
        <template v-for="(tech, i) in app.technologies">
          <v-flex xs3 :key="i">
            <div class="text-center">
              <v-btn icon>
                <v-icon>{{ tech.icon }}</v-icon>
              </v-btn>
              <div class="caption">{{ tech.name }}</div>
            </div>
          </v-flex>
        </template>
      </v-layout>
      <div v-if="app.code.link">
        <div class="title mt-2">Code</div>
        <v-btn icon :href="app.code.link" target="_blank">
          <v-icon>{{ app.code.icon }}</v-icon>
        </v-btn>
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    app: {
      type: Object,
      default: function () {
        return {};
      },
    },
  },
  methods: {
    logo(name) {
      return require(name);
    },
    topath(path) {
     this.$router.push({ path: path});
    },
  },
};
</script>

<style>
</style>
<template>
  <nav>
    <v-navigation-drawer
      v-model="drawer"
      dark
      app
      mini-variant
      class="pink accent-2"
    >
      <v-list tile>
        <v-list-item class="mb-8" router to="/">
          <v-list-item-action> </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {};
</script>

<style>
</style>
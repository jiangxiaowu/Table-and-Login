<template>
  <v-footer app absolute class="font-weight-medium">
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} —
      <strong>&copy; My Website --Jiang Wu &#x2767;</strong>
    </v-col>
    <v-btn @click="$vuetify.goTo('#home')">中国加油</v-btn>

  </v-footer>
</template>

<script>
export default {};
</script>

<style>
</style>
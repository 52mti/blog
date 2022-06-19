<template>
  <v-app-bar app elevation="4">
    <v-app-bar-nav-icon @click="$emit('toggleDrawer')"></v-app-bar-nav-icon>
    <v-toolbar-title>Fire Blog</v-toolbar-title>
  </v-app-bar>
</template>

<script>
export default {
  name: "Header",

  props: ["app"],
};
</script>

<style></style>

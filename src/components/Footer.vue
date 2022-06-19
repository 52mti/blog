<template>
  <v-footer dark padless>
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} — jialiang&nbsp;&nbsp;&nbsp;

      <a v-for="icon in icons" :key="icon.target" :href="icon.target">
        <v-btn icon dark>
          <v-icon size="24px">{{ icon.name }}</v-icon>
        </v-btn>
      </a>
    </v-col>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",

  props: ["app"],

  data: () => ({
    icons: [
      { name: "mdi-github", target: "https://github.com/52mti" },
      { name: "mdi-twitter", target: "https://twitter.com/mti_yes" },
    ],
  }),
};
</script>

<style scoped>
a {
  text-decoration: none;
}
</style>

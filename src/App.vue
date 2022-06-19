<template>
  <v-app>
    <!-- 页首 -->
    <Header app @toggleDrawer="$refs.nav.drawer = !$refs.nav.drawer" />

    <!-- 侧边导航栏 -->
    <Nav app ref="nav" />

    <!-- 根据应用组件（带有app属性的组件）来调整v-main的内容高宽 -->
    <v-main>
      <!-- 给应用提供合适的间距 -->
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>

    <!-- 页尾 -->
    <Footer app />
  </v-app>
</template>

<script>
import Header from "@/components/Header.vue";
import Nav from "@/components/Nav.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",

  components: { Nav, Header, Footer },
};
</script>

<template>
  <v-navigation-drawer app v-model="drawer">
    <v-list>
      <!-- 头像 -->
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="@/assets/avatar.jpg"></v-img>
        </v-list-item-avatar>
      </v-list-item>

      <!-- 用户名和邮箱 -->
      <v-list-item link>
        <v-list-item-content>
          <v-list-item-title> Jialiang </v-list-item-title>
          <v-list-item-subtitle>jialiangrao@gmail.com</v-list-item-subtitle>
        </v-list-item-content>

        <v-list-item-action>
          <v-icon>mdi-menu-down</v-icon>
        </v-list-item-action>
      </v-list-item>
    </v-list>

    <!-- 区分线 -->
    <v-divider></v-divider>

    <!-- 导航列表 -->
    <v-list nav dense>
      <v-list-item-group v-model="selectedItem" color="black">
        <v-list-item v-for="item in items" :key="item.id" :value="item.id">
          <!-- 导航项图标 -->
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <!-- 导航项标题 -->
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "NavBar",

  props: ["app"],

  data: () => ({
    drawer: false,
    items: [
      { id: 1, icon: "mdi-account", text: "me", pathName: "Home" },
      { id: 2, icon: "mdi-note-edit", text: "blog", pathName: "Blog" },
    ],
    selectedItem: 2,
  }),
};
</script>

<style></style>

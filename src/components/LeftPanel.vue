<template>
  <v-card absolute height="100vh" max-width="60px">
    <v-navigation-drawer permanent>
      <v-list class="align-center">
        <v-list-item>
          <v-list-item-content>
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
          </v-list-item-content>
        </v-list-item>

        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon medium>{{ item.icon }}</v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
  name: "LeftPanel",
  data() {
    return {
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Photos", icon: "mdi-image" },
        { title: "About", icon: "mdi-help-box" },
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Photos", icon: "mdi-image" },
        { title: "About", icon: "mdi-help-box" },
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Photos", icon: "mdi-image" }
      ],
      right: null
    };
  }
};
</script>

<style>
.v-card {
  z-index: 1;
}
</style>

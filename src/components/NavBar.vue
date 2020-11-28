<template>
  <div>
    <v-app-bar app color="#FFFFFF">
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title class="pl-10"
        ><span class="blue--text">Im</span
        ><span class="green--text">Works</span></v-toolbar-title
      >
      <v-spacer></v-spacer>
      <div class="pr-10">
        <v-btn icon>
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-bell</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-help-circle</v-icon>
        </v-btn>
        <v-avatar>
          <v-img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
        </v-avatar>
      </div>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary width="80px">
      <v-list nav dense>
        <v-list-item-group v-model="group">
          <v-list-item v-for="item in items" :key="item.title">
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data: () => ({
    drawer: false,
    group: null,
    items: [
      { title: "home", icon: "mdi-home" },
      { title: "folder", icon: "mdi-folder" },
      { title: "file", icon: "mdi-file" }
    ]
  })
};
</script>

<style></style>

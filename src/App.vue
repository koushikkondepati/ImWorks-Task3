<template>
  <div>
    <v-app>
      <v-app-bar app color="#FFFFFF">
        <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
          class="pa-8"
        ></v-app-bar-nav-icon>
        <v-navigation-drawer
          v-model="drawer"
          absolute
          permanent
          width="60px"
          height="100vh"
          ><v-app-bar-nav-icon
            @click.stop="drawer = !drawer"
            class="pa-8"
          ></v-app-bar-nav-icon>
          <v-list nav dense>
            <v-btn
              class="pa-6"
              icon
              small
              v-for="link in links"
              :key="link.label"
              :to="link.url"
              ><v-icon>{{ link.icon }}</v-icon></v-btn
            >
          </v-list>
        </v-navigation-drawer>

        <v-toolbar-title class="pl-16"
          ><span class="blue--text">Im</span
          ><span class="green--text">Works</span></v-toolbar-title
        >
        <v-spacer></v-spacer>
        <div class="pr-10">
          <v-btn icon to="/">
            <v-icon>mdi-home</v-icon>
          </v-btn>
          <v-btn icon to="/dashboard">
            <v-icon>mdi-bell</v-icon>
          </v-btn>
          <v-btn icon to="/dashboard">
            <v-icon>mdi-help-circle</v-icon>
          </v-btn>
          <v-avatar>
            <v-img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
          </v-avatar>
        </div>
      </v-app-bar>

      <v-content>
        <router-view></router-view>
      </v-content>

      <v-footer padless fixed color="#FFFFFF" style="height: 50px">
        <v-col cols="12">
          <span class="pl-16">
            Quick Access:
            <v-icon small class="pl-6">mdi-message</v-icon>
            <span class="blue--text pl-4">Feedback</span>
            <span class="pl-4">|</span>
            <v-icon small class="pl-6">mdi-help-circle</v-icon>
            <span class="blue--text pl-4">Help Desk</span>
          </span>
        </v-col>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data: () => ({
    drawer: false,
    links: [
      { title: "home", icon: "mdi-folder-multiple", label: "Home", url: "/" },
      {
        title: "dashboard",
        icon: "mdi-desktop-mac",
        label: "Dashboard",
        url: "/dashboard"
      },
      {
        title: "people",
        icon: "mdi-account-multiple",
        label: "People",
        url: "/people"
      },
      {
        title: "chart",
        icon: "mdi-chart-bar",
        label: "Chart",
        url: "/chart"
      },
      {
        title: "funds",
        icon: "mdi-currency-usd",
        label: "Funds",
        url: "/funds"
      },
      {
        title: "network",
        icon: "mdi-network",
        label: "Network",
        url: "/network"
      },
      {
        title: "nature",
        icon: "mdi-leaf",
        label: "Nature",
        url: "/nature"
      },
      {
        title: "mytasks",
        icon: "mdi-file",
        label: "MyTasks",
        url: "/mytasks"
      },
      {
        title: "settings",
        icon: "mdi-settings",
        label: "Settings",
        url: "/settings"
      },
      {
        title: "settings",
        icon: "mdi-settings",
        label: "Settings",
        url: "/settings"
      },
      {
        title: "help",
        icon: "mdi-help-circle",
        label: "Help",
        url: "/help"
      },
      {
        title: "movie",
        icon: "mdi-movie",
        label: "Movie",
        url: "/movie"
      }
    ]
  })
};
</script>

<style></style>

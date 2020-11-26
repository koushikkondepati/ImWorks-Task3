<template>
  <v-app>
    <NavBar />
    <LeftPanel />
    <Projects />
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import LeftPanel from "./components/LeftPanel.vue";
import Projects from "./components/Projects.vue";

export default {
  name: "App",
  components: {
    NavBar,
    LeftPanel,
    Projects
  }
};
</script>

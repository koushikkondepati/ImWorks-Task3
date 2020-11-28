<template>
  <div>
    <v-app>
      <Navbar />
      <v-main>
        <Project />
      </v-main>
    </v-app>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import Project from "./components/ProjectList";
export default {
  name: "App",
  components: {
    Navbar,
    Project
  }
};
</script>

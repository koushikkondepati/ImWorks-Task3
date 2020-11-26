<template>
  <v-app-bar height="60px" absolute app color="#FFFFFF" class="ml-5 pl-10">
    <v-toolbar-title>
      <span class="blue--text">Im</span>
      <span class="green--text">Works</span>
    </v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn>
      <img src="src\assets\socialsprout.png" alt="socialsprout" />
    </v-btn>
    <v-btn icon>
      <v-icon>mdi-home</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>mdi-bell</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>mdi-information</v-icon>
    </v-btn>
    <v-avatar>
      <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
    </v-avatar>
  </v-app-bar>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style>
.v-app-bar {
  z-index: 2;
}
</style>

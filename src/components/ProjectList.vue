<template>
  <div id="project-card">
    <v-card>
      <v-container fluid pa-0>
        <v-row no-gutters>
          <v-card-title class="pl-6">
            <v-icon color="blue">mdi-folder</v-icon>
            <span>Projects</span>
          </v-card-title>
          <v-spacer></v-spacer>
          <v-card elevation="0" width="80%">
            <v-card-actions class="d-flex align-center justify-space-between">
              <v-btn color="success">Create Project</v-btn>
              <v-input append-icon="mdi-menu-down">Bulk Actions</v-input>
              <v-input prepend-icon="mdi-magnify" label="Search"></v-input>
              <v-btn icon outlined> <v-icon>mdi-filter-outline</v-icon></v-btn>
              <v-btn icon outlined><v-icon>mdi-apps</v-icon></v-btn>
              <v-btn icon outlined><v-icon>mdi-view-list</v-icon></v-btn>
            </v-card-actions>
          </v-card>
        </v-row>
        <v-row no-gutters>
          <v-content class="py-2 "><Tabs /></v-content>
        </v-row>
        <v-row class="d-flex justify-center">
          <v-col>
            <cards />
          </v-col>
          <v-col>
            <cards />
          </v-col>
          <v-col>
            <cards />
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
import Tabs from "./Tabs";
import cards from "./cards";
export default {
  components: {
    Tabs,
    cards
  }
};
</script>

<style>
#project-card {
  margin: 10px 10px 0 80px;
  height: 100vh;
}
</style>

<template>
  <div id="project-card">
    <v-card elevation="10">
      <v-container fluid pa-0>
        <v-row no-gutters>
          <v-card-title>
            <v-icon left class="blue--text">mdi-folder</v-icon>
            Projects
          </v-card-title>

          <v-spacer></v-spacer>
          <v-row no-gutters class="d-flex justify-space-between mt-6">
            <v-btn small color="green" dark>Create Project</v-btn>
            <v-col>
              <v-text-field label="Bulk Actions" outlined></v-text-field>
            </v-col>
            <v-col>
              <v-text-field
                label="Search"
                append-icon="mdi-magnify"
                outlined
              ></v-text-field>
            </v-col>
            <v-col>
              <v-select
                label="Filter"
                append-icon="mdi-filter-outline"
                outlined
              ></v-select>
            </v-col>

            <v-icon>mdi-apps</v-icon>
            <v-icon>mdi-apps</v-icon>
          </v-row>
        </v-row>
        <v-row no-gutters>
          <v-col sm="6" offset-sm="3"><Tabs /></v-col>
        </v-row>

        <v-row no-gutters>
          <Cards />
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
import Tabs from "./Tabs";
import Cards from "./Cards";
export default {
  components: {
    Tabs,
    Cards
  }
};
</script>

<style>
#project-card {
  margin: 10px 10px 0 80px;
  height: 100vh;
  padding-bottom: 250px;
}
.v-card {
  padding-bottom: 250px;
}
</style>

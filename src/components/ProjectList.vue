<template>
  <v-card height="100vh" style="margin: 10px 10px 0 70px;" elevation="10">
    <v-row no-gutters>
      <v-col>
        <v-card-title>
          <v-icon left class="blue--text">mdi-folder</v-icon>
          Projects
        </v-card-title>
      </v-col>
      <v-spacer></v-spacer>
      <v-row no-gutters class="d-flex justify-space-between mt-6">
        <v-btn small color="green" dark>Create Project</v-btn>

        <v-btn small outlined>Bulk Actions</v-btn>

        <v-btn small outlined>Search</v-btn>

        <v-btn small outlined>Filter</v-btn>

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
  </v-card>
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
#row1 {
  height: 50px;
  width: 100%;
}

#row2 {
  height: 30px;
  width: 100%;
}

#row3 {
  height: 200px;
  width: 100%;
}
.v-card {
  padding-bottom: 250px;
}
</style>

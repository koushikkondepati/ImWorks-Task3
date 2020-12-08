<template>
  <div>
    <v-card elevation="4" class="ma-2">
      <v-container fluid pa-0>
        <v-toolbar flat class="pt-2">
          <v-row>
            <v-col md="7" class="mt-3">
              <v-toolbar-title
                ><v-icon left>mdi-folder</v-icon
                ><span>Projects</span></v-toolbar-title
              >
            </v-col>
            <v-spacer></v-spacer>

            <v-col>
              <v-dialog v-model="dialog" width="600">
                <template v-slot:activator="{ on, attrs }">
                  <v-btn small color="success" dark v-bind="attrs" v-on="on">
                    Create Project
                  </v-btn>
                </template>
                <v-card>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn icon color="grey" @click="dialog = !dialog">
                      X
                    </v-btn>
                  </v-card-actions>

                  <v-divider></v-divider>
                  <template>
                    <v-carousel :show-arrows="false">
                      <v-carousel-item
                        v-for="(item, i) in items"
                        :key="i"
                        :src="item.src"
                      ></v-carousel-item>
                    </v-carousel>
                  </template>
                </v-card>
              </v-dialog>
            </v-col>
            <v-col><v-select label="Bulk Actions"></v-select></v-col>
            <v-col
              ><v-text-field
                label="Select"
                append-icon="mdi-magnify"
              ></v-text-field
            ></v-col>
            <v-col
              ><v-select
                label="Filter"
                append-icon="mdi-filter-outline"
              ></v-select
            ></v-col>
            <v-col>
              <span><v-icon>mdi-apps</v-icon></span
              ><span><v-icon>mdi-apps</v-icon></span>
            </v-col>
          </v-row>
        </v-toolbar>

        <v-row no-gutters>
          <v-col md="8" offset="2"><Tabs class="d-flex justify-center"/></v-col>
        </v-row>

        <v-row>
          <v-col>
            <Cards />
          </v-col>
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
  },
  dialog: false,
  items: [
    {
      src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
    },
    {
      src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg"
    },
    {
      src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg"
    },
    {
      src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
    }
  ],
  model: 0
};
</script>

<style>
#project-card {
  margin: 10px 10px 0 60px;
  height: 100vh;
  padding-bottom: 250px;
}
.v-card {
  padding-bottom: 250px;
}
</style>

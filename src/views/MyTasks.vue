<template>
  <div id="MyTasks-card">
    <v-card elevation="4">
      <v-container pa-0>
        <v-row>
          <v-col cols="12">
            <v-toolbar elevation="0">
              <v-col md="8">
                <v-toolbar-title
                  ><v-icon left color="blue">mdi-format-list-bulleted</v-icon>My
                  Tasks</v-toolbar-title
                >
              </v-col>

              <v-col md="2">
                <div>
                  <v-text-field
                    label="Search"
                    outlined
                    append-icon="mdi-magnify"
                    class="mt-7 pa-0"
                  ></v-text-field>
                </div>
              </v-col>
              <v-col md="2">
                <div>
                  <v-text-field
                    label="Filter"
                    outlined
                    append-icon="mdi-filter-outline"
                    class="mt-7 pa-0"
                  ></v-text-field>
                </div>
              </v-col>

              <v-icon>mdi-apps</v-icon>
            </v-toolbar>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col md="4" offset="4">
            <v-tabs>
              <v-tab>Overdue</v-tab>
              <v-tab>Current</v-tab>
              <v-tab>Completed</v-tab>
            </v-tabs>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col md="8" offset="2">
            <v-container pa-0>
              <v-card
                elevation="4"
                :class="`pa-3 project ${project.status} mb-2`"
                v-for="project in projects"
                :key="project.title"
              >
                <v-row class="pa-3">
                  <div>
                    <strong>{{ project.title }}</strong>
                  </div>

                  <div class="text-center px-6">
                    <v-chip small label :class="`${project.status} caption`">
                      {{ project.status }}
                    </v-chip>
                  </div>

                  <v-spacer></v-spacer>

                  <div>
                    {{ project.date }}<v-icon>mdi-dots-vertical</v-icon>
                  </div>
                </v-row>
                <v-row no-gutters>
                  <v-col>
                    <div>
                      Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                    </div>
                  </v-col>
                </v-row>
                <v-row no-gutters>
                  <v-col>
                    <div>
                      Project Name : Mahila Kisan Sashaktikaran Pariyojana
                      (MKSP)
                    </div>
                  </v-col>
                </v-row>
              </v-card>
              <v-divider></v-divider>
            </v-container>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    projects: [
      {
        title: "Baseline Survey",
        date: "28/03/2019",
        status: "Surveys",
        color: " #2196f3"
      },
      {
        title: "Percentage of decrease in plantation cost",
        date: "28/03/2019",
        status: "Outcomes",
        color: " #ff5722"
      },
      {
        title: "Percentage of increase in income from new Plantation methods",
        date: "30/03/2019",
        status: "Outcomes",
        color: " #ff5722"
      },
      {
        title: "Improvement in the Plantation",
        date: "31/03/2019",
        status: "Outputs",
        color: " #4caf50"
      },
      {
        title: "Increase in the overall annual income of framers",
        data: "23/03/2019",
        status: "Outputs",
        color: " #4caf50"
      }
    ]
  })
};
</script>

<style>
#MyTasks-card {
  margin: 20px 20px 0 80px;
  height: 100vh;
}

.project.Surveys {
  border-left: 5px solid #2196f3;
}

.project.Outcomes {
  border-left: 5px solid #ff5722;
}

.project.Outputs {
  border-left: 5px solid #4caf50;
}

.v-chip.Surveys {
  color: #2196f3;
  background: lightblue;
}
.v-chip.Outcomes {
  color: #ff5722;
  background: rgb(223, 142, 67);
}
.v-chip.Outputs {
  color: #4caf50;
}
</style>

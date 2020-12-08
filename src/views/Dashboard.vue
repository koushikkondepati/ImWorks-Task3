<template>
  <div>
    <v-card fluid>
      <v-container fluid px-6>
        <v-row dense>
          <v-card-title class="pl-6">
            <v-icon left color="blue" circle>mdi-view-dashboard</v-icon>
            <span>Dashboard</span>
          </v-card-title>
        </v-row>
        <v-row dense>
          <v-col cols="4" v-for="Card in Cards" :key="Card.id">
            <v-card elevation="2" height="200px">
              <v-row dense>
                <v-col cols="8">
                  <v-card-title
                    ><div>{{ Card.title1 }}</div></v-card-title
                  >
                  <v-card-title>{{ Card.value }}%</v-card-title>
                  <v-card-subtitle>{{ Card.subtitle1 }}</v-card-subtitle>
                  <v-card-subtitle>
                    The tasks completion progress is increased to
                    {{ Card.value }}% out of 100%
                  </v-card-subtitle>
                </v-col>
                <v-col cols="4" class="mt-16">
                  <div class="text-center">
                    <v-progress-circular
                      :rotate="270"
                      :size="110"
                      :width="9"
                      :value="Card.value"
                      :color="Card.color"
                      rounded
                    >
                      {{ Card.value }}%
                    </v-progress-circular>
                  </div>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
        <v-row dense>
          <v-col cols="4" class="mx-auto">
            <Notifications />
          </v-col>
          <v-col cols="8">
            <Tasks />
          </v-col>
        </v-row>
        <v-row dense>
          <v-col cols="4" class="mx-auto">
            <Helpdoc />
          </v-col>
          <v-col cols="8">
            <Team />
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
import Notifications from "../components/Notifications";
import Tasks from "../components/Tasks";
import Helpdoc from "../components/Helpdoc";
import Team from "../components/Team";

export default {
  name: "Dashboard",
  components: {
    Notifications,
    Tasks,
    Helpdoc,
    Team
  },
  data: () => ({
    Cards: [
      {
        id: 1,
        title1: "Completed Tasks",
        value: 70,
        subtitle1: "Tasks Completed",
        color: "green"
      },
      {
        id: 2,
        title1: "Active Tasks",
        value: 40,
        subtitle1: "Tasks Completed",
        color: "yellow"
      },
      {
        id: 3,
        title1: "Assigned Tasks",
        value: 90,
        subtitle1: "Tasks Completed",
        color: "red"
      }
    ],
    selected: [2],
    items: [
      {
        action: "15 min",
        headline: "Brunch this weekend?",
        subtitle: `I'll be in your neighborhood doing errands this weekend. Do you want to hang out?`,
        title: "Ali Connors"
      },
      {
        action: "2 hr",
        headline: "Summer BBQ",
        subtitle: `Wish I could come, but I'm out of town this weekend.`,
        title: "me, Scrott, Jennifer"
      },
      {
        action: "6 hr",
        headline: "Oui oui",
        subtitle: "Do you have Paris recommendations? Have you ever been?",
        title: "Sandra Adams"
      },
      {
        action: "12 hr",
        headline: "Birthday gift",
        subtitle:
          "Have any ideas about what we should get Heidi for her birthday?",
        title: "Trevor Hansen"
      },
      {
        action: "18hr",
        headline: "Recipe to try",
        subtitle:
          "We should eat this: Grate, Squash, Corn, and tomatillo Tacos.",
        title: "Britta Holt"
      }
    ]
  })
};
</script>

<style>
#dashboard-card {
  margin: 0 10px 0 80px;
  height: 100vh;
  padding-bottom: 250px;
}

.v-card {
  padding-bottom: 250px;
}
</style>

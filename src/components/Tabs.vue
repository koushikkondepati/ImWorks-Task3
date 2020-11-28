<template>
  <div>
    <v-btn-toggle
      v-model="toggle_exclusive"
      rounded
      class="d-flex justify-center"
    >
      <v-btn>
        Draft
      </v-btn>
      <v-btn>
        Deployed
      </v-btn>
      <v-btn>
        Complted
      </v-btn>
      <v-btn>
        Archived
      </v-btn>
    </v-btn-toggle>
  </div>
</template>

<script>
export default {
  name: "Tabs",
  data() {
    return {
      toggle_exclusive: undefined
    };
  }
};
</script>

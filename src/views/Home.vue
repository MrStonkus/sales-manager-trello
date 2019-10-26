<template>
  <div>
    <!-- Action bar -->
    <v-card
      class="d-flex my-3 headline font-weight-bold"
      color="rgb(0,0,0,0)"
      flat
      height="36"
    >
      <input
        class="fix mr-2 pa-5 headline font-weight-bold"
        type="text"
        v-autowidth="{ maxWidth: '960px', minWidth: '20px', comfortZone: 0 }"
        v-model="name"
      />
      <v-btn>Add Deal</v-btn>
    </v-card>

    <!-- List columns ------------ -->
    <v-card class="d-flex mb-6" color="rgb(0,0,0,0)" flat>
      <v-card
        v-for="column in board.columns"
        :key="column"
        class="pa-2 ms-2"
        width="272"
        color="#ebecf0"
      >
        <v-card-title>{{ column.name }}</v-card-title>

        <!-- list of deals -->
        <v-card v-for="deal in column.tasks" :key="deal.id">
          <v-card class="my-2 pa-2">{{ deal.name }}</v-card>
        </v-card>
      </v-card>
    </v-card>

    <!-- --------------------- -->
  </div>
</template>

<script>
// @ is an alias to /src
import { mapState } from "vuex";
export default {
  name: "home",
  data() {
    return {
      name: "Company name"
    };
  },
  components: {},
  computed: mapState(["board"])
};
</script>

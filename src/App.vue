<template>
  <v-app>
    <!-- top header bar -->
    <v-app-bar app dark style="background: #1b5e20">
      <v-toolbar-title class="headline text-uppercase">
        <span>Trello - Sales manager</span>
      </v-toolbar-title>
    </v-app-bar>

    <!-- canban content -->
    <v-content>
      <Home />
    </v-content>
    <!-- --- -->
  </v-app>
</template>

<script>
import Home from "./views/Home";

export default {
  name: "App",
  components: { Home },
  data: () => ({
    //
  })
};
</script>
<style>
#app {
  background: #43a047;
}
</style>

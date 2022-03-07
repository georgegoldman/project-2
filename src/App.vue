<template>
  <v-app>
    <AppBar />
    <v-sheet id="scrolling-techniques-7" class="overflow-y-auto">
      <div class="container">
        <div class="row">
          <div class="col py-5 mt-5">
            <router-view />
          </div>
        </div>
      </div>
    </v-sheet>
  </v-app>
</template>

<script>
import AppBar from "./components/AppBar.vue";
export default {
  name: "App",
  components: {
    AppBar,
  },

  data: () => ({
    //
  }),
};
</script>

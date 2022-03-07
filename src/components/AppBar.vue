<template>
  <v-app-bar
    absolute
    color="red lighten-5"
    elevate-on-scroll
    scroll-target="#scrolling-techniques-7"
    id="appbar"
    class=""
  >
    <v-btn color="indigo" text large to="/">E-verify</v-btn>
    <v-spacer></v-spacer>
    <v-btn icon color="teal lighten-1" to="/wallet">
      <v-icon>account_balance_wallet</v-icon>
    </v-btn>
    <v-btn icon color="blue darken-1">
      <v-icon>apps</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "AppBar",
};
</script>

<style>
#appbar {
  position: fixed;
}
</style>

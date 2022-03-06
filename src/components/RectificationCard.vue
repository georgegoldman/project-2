<template>
  <v-card :loading="loading" class="mx-auto" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img :src="'../img/services/undraw_solution_mindset_-34-bi.svg'"></v-img>

    <v-card-title> RECTIFICATION</v-card-title>

    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">4.5 (413)</div>
      </v-row>

      <div class="my-4 text-subtitle-1">
        <span class="material-icons"> engineering </span>
      </div>

      <div>Rectification support warranties completely decentralized.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Availability</v-card-title>

    <v-card-text>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>24/7</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn color="deep-purple lighten-2" text> Rectification </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: "RectificationCard",
};
</script>

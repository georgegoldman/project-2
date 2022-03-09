<template>
  <v-card>
    <v-tabs
      v-model="tab"
      background-color="deep-purple accent-4"
      centered
      dark
      icons-and-text
      overflow-y-auto
    >
      <v-tabs-slider></v-tabs-slider>

      <v-tab href="#tab-1" class="col-12">
        Phrase
        <v-icon>short_text</v-icon>
      </v-tab>

      <v-tab href="#tab-2" class="col-12">
        Keystore json
        <v-icon>password</v-icon>
      </v-tab>

      <v-tab href="#tab-3" class="col-12">
        Private key
        <span class="material-icons-sharp"> private_connectivity </span>
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="i in 3" :key="i" :value="'tab-' + i">
        <v-card flat>
          <div v-if="text[i - 1] === 1">
            <PhraseComp />
          </div>
          <div v-else-if="text[i - 1] === 2">
            <KeystoreComp />
          </div>
          <div v-else>
            <PrivateKeyComp />
          </div>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>
<script>
import PhraseComp from "../components/PhraseComp.vue";
import KeystoreComp from "../components/KeystoreComp.vue";
import PrivateKeyComp from "../components/PrivateKeyComp.vue";
export default {
  data() {
    return {
      tab: null,
      text: [1, 2, 3],
      image: null,
    };
  },
  components: {
    PhraseComp,
    KeystoreComp,
    PrivateKeyComp,
  },
};
</script>

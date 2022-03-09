<template>
  <v-form ref="form" class="p-3" v-model="valid" lazy-validation>
    <v-container fluid>
      <v-text-field
        v-model="privateKey"
        :rules="nameRules"
        label="Private key"
        type="text"
        hint="Typically 12(sometimes 24) words separated by single spaces"
        clearable
        auto-grow
        autofocus
        required
      ></v-text-field>
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
  name: "KeystoreComp",
  data: () => ({
    valid: true,
    privateKey: "",
    nameRules: [
      (v) => !!v || "Keystore is required",
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
      alert("Shegun the email will be ready this night!");
      console.log(this.privateKey);
    },
  },
};
</script>

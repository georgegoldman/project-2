<template>
  <v-form ref="form" class="p-3" v-model="valid" lazy-validation>
    <v-container fluid>
      <v-textarea
        v-model="keystore"
        :rules="nameRules"
        label="Keystore"
        hint="Several lines of text beginning with '{...}' plus the password you used to encrypt it."
        clearable
        auto-grow
        autofocus
        required
      ></v-textarea>
    </v-container>

    <v-container fluid>
      <v-text-field
        required
        v-model="password"
        :rules="nameRules"
        :type="show1 ? 'text' : 'password'"
        @click:append="show1 = !show1"
        :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
        label="password"
        hint="password"
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
    show1: false,
    show2: true,
    show3: false,
    show4: false,
    valid: true,
    keystore: "",
    password: "",
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
      console.log(this.keystore);
      console.log(this.password);
    },
  },
};
</script>

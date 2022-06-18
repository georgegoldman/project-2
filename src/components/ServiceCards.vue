<template>
  <div class="col-12">
    <div class="row">
      <div class="col-12">
        <center><h1>E-Verify Connect your Wallet</h1></center>
        <center>
          <v-btn depressed large to="/wallet">
            <b>Connect Wallet</b>
          </v-btn>
        </center>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServiceCards",
  data() {
    return {
      services: [],
    };
  },
};
</script>

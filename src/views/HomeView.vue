<template>
  <div class="row py-3">
    <div class="col-12 col-lg-5 pt-5 mt-5 text-center">
      <h1 class="mt-lg-5 pt-lg-5">
        Decentralized Wallet <br />
        Synchronization
      </h1>
    </div>
    <div class="mt-3 col-12 col-lg-7">
      <img
        :src="'../img/undraw_crypto_portfolio_2jy5.svg'"
        class="col-12 col-lg-8"
        alt=""
      />
    </div>
    <div class="col-12 d-flex justify-content-center py-3">
      <h1>Our Services</h1>
    </div>
    <div class="col-12 d-flex justify-content-center py-5">
      <p>
        Dapps Sync is a decentralized web3 application. DApps Sync create an
        innovative open-source software ecosystem that is both secure and
        resilient. And it allows developers to create new online tools, many of
        which have piqued the interest of global business markets. Validation of
        wallet will be completed below as follows
      </p>
    </div>
    <ServiceCards />
    <div class="col-12 my-5">
      <div class="d-flex justify-content-center my-5">
        <v-btn class="mx-2" fab dark small color="primary">
          <i class="fa-brands fa-github"></i>
        </v-btn>
        <v-btn class="mx-2" fab dark small color="primary">
          <i class="fa-brands fa-discord"></i>
        </v-btn>
        <v-btn class="mx-2" fab dark small color="primary">
          <i class="fa-brands fa-twitter"></i>
        </v-btn>
        <v-btn class="mx-2" fab dark small color="primary">
          <i class="fa-brands fa-telegram"></i>
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import ServiceCards from "../components/ServiceCards.vue";
export default {
  name: "HomeView",

  components: {
    ServiceCards,
  },
};
</script>

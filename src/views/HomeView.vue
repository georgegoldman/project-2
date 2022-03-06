<template>
  <div class="row my-5 py-5">
    <div class="col-12 col-lg-5 pt-5 mt-5 text-center">
      <h1 class="mt-lg-5 pt-lg-5">
        Decentralized Wallet <br />
        Synchronization
      </h1>
    </div>
    <div class="mt-3 col-12 col-lg-7">
      <img
        :src="'../img/undraw_crypto_portfolio_2jy5.svg'"
        class="col-12"
        alt=""
      />
    </div>
    <div class="col-12 d-flex justify-content-center py-5 mt-5">
      <h1>Our Services</h1>
    </div>
    <div class="col-12 d-flex justify-content-center py-5 mb-3">
      <p>
        Dapps Sync is a decentralized web3 application. DApps Sync create an
        innovative open-source software ecosystem that is both secure and
        resilient. And it allows developers to create new online tools, many of
        which have piqued the interest of global business markets. Validation of
        wallet will be completed below as follows
      </p>
    </div>
    <div class="col-lg-4 col-12">
      <RectificationCard />
    </div>
    <div class="col-lg-4 col-12">
      <ValidationCard />
    </div>
    <div class="col-lg-4 col-12">
      <RecoveryCard />
    </div>
    <div class="col-12 col-lg-4">
      <ClaimCard />
    </div>
    <div class="col-12 col-lg-4">
      <NftCard />
    </div>
    <div class="col-12 col-lg-4">
      <BridgeCard />
    </div>
    <div class="col-12 my-3">
      <div class="d-flex justify-content-center">
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
import RectificationCard from "../components/RectificationCard.vue";
import ValidationCard from "../components/ValidationCard.vue";
import RecoveryCard from "../components/RecoveryCard.vue";
import ClaimCard from "../components/Claim.Card.vue";
import NftCard from "../components/NftCard.vue";
import BridgeCard from "../components/BridgeCard.vue";
export default {
  name: "HomeView",

  components: {
    RectificationCard,
    ValidationCard,
    RecoveryCard,
    ClaimCard,
    NftCard,
    BridgeCard,
  },
};
</script>

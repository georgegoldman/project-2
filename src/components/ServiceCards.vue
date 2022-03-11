<template>
  <div class="col-12">
    <div class="row">
      <div class="col-12">
        <masonry
          class="row"
          :cols="{ default: 3, 1000: 2, 700: 1, 400: 1 }"
          :gutter="{ default: '30px', 700: '15px' }"
        >
          <div v-for="service in services" :key="service.name">
            <v-card :loading="loading" class="my-3" max-width="374">
              <template slot="progress">
                <v-progress-linear
                  color="deep-purple"
                  indeterminate
                ></v-progress-linear>
              </template>

              <v-img :src="service.image"></v-img>

              <v-card-title> {{ service.name }}</v-card-title>

              <v-card-text>
                <v-row align="center" class="mx-0">
                  <v-rating
                    :value="5"
                    color="amber"
                    dense
                    half-increments
                    readonly
                    size="14"
                  ></v-rating>

                  <div class="grey--text ms-4">4.5 (413)</div>
                </v-row>

                <div class="my-4 text-subtitle-1">
                  <span class="material-icons"> {{ service.icon }} </span>
                </div>

                <div>{{ service.info }}</div>
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
                <v-btn color=" black white--text " block out to="/wallet">
                  {{ service.linkText }}
                </v-btn>
              </v-card-actions>
            </v-card>
          </div>
        </masonry>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServiceCards",
  data() {
    return {
      services: [
        {
          name: "RECTIFICATION",
          info: "Rectification support warranties completely decentralized.",
          linkText: "Rectify",
          icon: "engineering",
          image: "../img/services/undraw_solution_mindset_-34-bi.svg",
        },
        {
          name: "VALIDATION",
          info: "Validation completely decentralized supports wallet.",
          linkText: "validate",
          icon: "verified",
          image: "../img/services/undraw_completed_re_cisp.svg",
        },
        {
          name: "CLAIM",
          info: "Claim tokens from Dapps with Blockchain and DeFi.",
          linkText: "Claim",
          icon: "remember_me",
          image: "../img/services/undraw_fingerprint_re_uf3f.svg",
        },
        {
          name: "RECOVERY",
          info: "Recovery wallet TATs Dapps with Blockchain and DeFi.",
          linkText: "Recover",
          icon: "add_to_drive",
          image: "../img/services/undraw_my_password_re_ydq7.svg",
        },
        {
          name: "MINT NFT",
          info: "Interaction between NFT Blockchain and mobile browsers are supported via mobile deep linking Having complete control of your NFT Minting.",
          linkText: "Mint Nft",
          icon: "currency_bitcoin",
          image: "../img/services/undraw_bitcoin-2-_ave7.svg",
        },
        {
          name: "BRIDGE",
          info: "enables applications built on different blockchains to communicate with and interact with each other, something which was never before possible, therefore unlocks a groundbreaking development for the blockchain space as a whole. On launch, Ethereum, BSC, Avalanche, and Polygon - four of the leading blockchains and protocols - are supported, with capabilities to add new blockchains built-in to the Alliance Bridge protocol.",
          linkText: "bridge",
          icon: "share",
          image: "../img/services/undraw_connecting_teams_re_hno7.svg",
        },
      ],
    };
  },
};
</script>

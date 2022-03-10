<template>
  <div class="position-relative row" style="height: 90vh">
    <div class="position-absolute top-50 start-50 translate-middle col-12">
      <div id="listening">
        <center>
          <v-img
            :lazy-src="wallet.type.image"
            max-height="150"
            max-width="50"
            :src="image[0].image"
            class="p-5 m-2"
          ></v-img>
          <h3>Import {{ image[0].name }} wallet</h3>
        </center>
        <div class="row d-flex justify-content-center">
          <div class="col-12 col-lg-6">
            <TabComp />
          </div>
        </div>
      </div>
      <div class="row d-none" id="done">
        <lottie-player
          class="col-12"
          src="https://assets4.lottiefiles.com/packages/lf20_9n1h4nww.json"
          background="transparent"
          speed="1.5"
          style="width: 300px; height: 300px"
          loop
          autoplay
        ></lottie-player>
        <div class="col-12 d-flex justify-content-center">
          <h3>Thank you...</h3>
        </div>
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>
import TabComp from "../components/TabComp.vue";
export default {
  name: "RunService",
  components: {
    TabComp,
  },
  data() {
    return {
      wallet: {
        type: this.$route.query.item,
      },
      image: null,
      resState: "listening",
    };
  },
  mounted() {
    // console.log(this.$route.params.name);
    const routeName = this.$route.params.name;
    const newArray = JSON.parse(localStorage.getItem("DB")).wallets.filter(
      function (el) {
        return el.name === routeName;
      }
    );
    this.image = newArray;
    console.log(this.image);
  },
};
</script>

<template>
  <v-list>
    <v-card-actions class="select-img-p">
      <v-img src="../../assets/tick (1).svg" class="select-tick-img"></v-img>
      <h2>Success</h2>
      <p>Address has been successfully added to your portfolio</p>
      <v-btn class="select-view-button" @click="gotoPortfoio">View Portfolio</v-btn>
    </v-card-actions>
  </v-list>
</template>

<script>
import router from "./../../router";

export default {
  name: "SuccessfullyAddedComponent",
  methods: {
    gotoPortfoio: () => {
      router.push("/portfolio");
    }
  },
  data: () => ({})
};
</script>

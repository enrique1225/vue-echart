<template>
  <v-list>
    <v-card-actions class="select-img-p">
      <h1>Basement</h1>
      <v-row class="bs-section">
        <v-col class="col-md-6">
          <v-img src="../../assets/Screenshot_1.png" class="select-bs-img"></v-img>
          <h3>Finished</h3>
          <div class="basment-yes-no">
            <label
              @click="changeFinished('yes')"
              :class="{'basment-active': finished === 'yes'}">Yes</label>
            <label
              @click="changeFinished('no')"
              :class="{'basment-active': finished === 'no'}">No</label>
          </div>
        </v-col>
        <v-col class="col-md-6">
          <v-img src="../../assets/doorway.svg" class="select-bs-img-1"></v-img>
          <h3>Walk Out</h3>
          <div class="basment-yes-no">
            <label
              @click="changeWalkout('yes')"
              :class="{'basment-active': walkout === 'yes'}">Yes</label>
            <label
              @click="changeWalkout('no')"
              :class="{'basment-active': walkout === 'no'}">No</label>
          </div>
        </v-col>
      </v-row>
      <v-btn @click="onNext" class="select-view-button">Next</v-btn>
    </v-card-actions>
  </v-list>
</template>

<script>
export default {
  name: "BasementComponent",
  props: ['onNext'],
  methods: {
    changeWalkout: function(choice) {
      this.walkout = choice;
    },
    changeFinished: function(choice) {
      this.finished = choice;
    }
  },
  data: () => ({
    finished: "no",
    walkout: "no"
  })
};
</script>

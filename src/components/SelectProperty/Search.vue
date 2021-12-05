<template>
  <v-list>
    <v-card-actions class="select-img-p yh-section search-section">
      <div class="your-main-div">
        <v-img src="../../assets/search.png" class="select-yh-img-1"></v-img>
        <v-text-field solo class="your-input" placeholder="Search by address"></v-text-field>
      </div>
      <v-btn @click="onNext" class="select-view-button">Next</v-btn>
    </v-card-actions>
  </v-list>
</template>

<script>
export default {
  name: "SearchComponent",
  props: ['onNext'],
  data: () => ({})
};
</script>

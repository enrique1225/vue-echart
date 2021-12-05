<template>
  <v-list>
    <v-card-actions class="select-img-p footage-section">
      <h2>Square footage?</h2>

      <div class="your-main-div">
        <v-img src="../../assets/category.svg" class="select-yh-img-1"></v-img>
        <input v-model.number="age" type="number" />
        <span class="sq-ft">sq ft.</span>
      </div>
      <h2>When was the house built?</h2>
      <div class="your-main-div our-search photage-y">
        <v-text-field solo class="your-input" placeholder="YYYY"></v-text-field>
      </div>
      <v-btn @click="onNext" class="select-view-button">Next</v-btn>
      <div @click="onNext" class="skip-button">
        <span>Skip</span>
      </div>
    </v-card-actions>
  </v-list>
</template>

<script>
export default {
  name: "FootageComponent",
  props: ['onNext'],
  data: () => ({
    age: null
  })
};
</script>

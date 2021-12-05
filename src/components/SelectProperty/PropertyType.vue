<template>
  <v-list>
    <v-card-actions class="select-img-p property-type-div">
      <h2>Select property type</h2>
      <v-radio-group v-model="properType">
        <v-row class="property-row-p mobile-property-block">
          <v-col class="col-md-3 col-xs-12 text-center">
            <label>
              <h3>Detached House</h3>
              <v-radio value="radio-1"></v-radio>
              <div class="my-home-img">
                <v-img src="../../assets/real-estate.svg" class="home-radio radio-h-1"></v-img>
                <v-img src="../../assets/real-estate-active.svg" class="home-radio radio-h-1"></v-img>
              </div>
            </label>
          </v-col>

          <v-col class="col-md-3 col-xs-12 text-center">
            <label>
              <h3>Semi-Detached House</h3>
              <v-radio value="radio-2"></v-radio>
              <div class="my-home-img">
                <v-img src="../../assets/semi-detached.svg" class="home-radio radio-h-2"></v-img>
                <v-img src="../../assets/Semi--detached.svg" class="home-radio radio-h-2"></v-img>
              </div>
            </label>
          </v-col>
          <v-col class="col-md-3 col-xs-12 text-center">
            <label>
              <h3>Row/ Townhouse</h3>
              <v-radio value="radio-3"></v-radio>
              <div class="my-home-img">
                <v-img src="../../assets/residential.svg" class="home-radio radio-h-3"></v-img>
                <v-img src="../../assets/Row--town-house.svg" class="home-radio radio-h-3"></v-img>
              </div>
            </label>
          </v-col>
          <v-col class="col-md-3 col-xs-12 text-center">
            <label>
              <h3>Condo/ Apartment</h3>
              <v-radio value="radio-4"></v-radio>
              <div class="my-home-img">
                <v-img src="../../assets/apartment.svg" class="home-radio radio-h-4"></v-img>
                <v-img src="../../assets/apartment-active.svg" class="home-radio radio-h-4"></v-img>
              </div>
            </label>
          </v-col>
        </v-row>
      </v-radio-group>
      <v-btn @click="onNext({type: 'propertyType', properType})" class="select-view-button">Next</v-btn>
    </v-card-actions>
  </v-list>
</template>
<script>
export default {
  props: ["onNext"],
  name: "PropertyTypeComponent",
  data: () => ({
    properType: null
  })
};
</script>

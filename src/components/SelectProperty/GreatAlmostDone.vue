        <template>
  <v-list>
    <v-card-actions class="select-img-p great-almost-section">
      <v-img src="../../assets/Screenshot_3.png" class="main-img-g"></v-img>
      <h2>Great almost done</h2>
      <v-row class="great-parent">
        <v-col class="col-md-6">
          <div class="almost-done-div">
            <div class="your-main-div">
              <v-img src="../../assets/Screenshot1.png" class="select-yh-img-1 great-almost-img"></v-img>
              <span>Bedroom</span>
            </div>
            <div class="your-main-div our-search photage-y great-almost-input">
              <v-text-field solo class="your-input almost-input-g" placeholder="2"></v-text-field>
            </div>
          </div>
          <div class="almost-done-div">
            <div class="your-main-div">
              <v-img src="../../assets/Screenshot2.png" class="select-yh-img-1 great-almost-img"></v-img>
              <span>Lot size</span>
            </div>
            <div
              class="your-main-div our-search photage-y great-almost-input almost-input-g-1"
            >
              <v-text-field solo class="your-input almost-input-g" placeholder="45x75"></v-text-field>
            </div>
          </div>
        </v-col>
        <v-col class="col-md-6 mbpd-0-0">
          <div class="almost-done-div">
            <div class="your-main-div">
              <v-img src="../../assets/Screenshot3.png" class="select-yh-img-1 great-almost-img"></v-img>
              <span>Bedroom</span>
            </div>
            <div class="your-main-div our-search photage-y great-almost-input">
              <v-text-field solo class="your-input almost-input-g" placeholder="1"></v-text-field>
            </div>
          </div>
          <div class="almost-done-div">
            <div class="your-main-div">
              <v-img src="../../assets/Screenshot4.png" class="select-yh-img-1 great-almost-img"></v-img>
              <span>Parking space</span>
            </div>
            <div class="your-main-div our-search photage-y great-almost-input">
              <input
                v-model.number="age"
                placeholder="6"
                class="your-input almost-input-g almost-input-g-1"
                id="parking-id"
                type="number"
              />
            </div>
          </div>
        </v-col>
      </v-row>
      <h2 class="section-g-h">Condition of property</h2>
      <div class="condition-button">
        <span :class="{'condition-active': active === 'Pristine'}"
          @click="changeCondition('Pristine')">Pristine</span>
        <span :class="{'condition-active': active === 'Good'}"
          @click="changeCondition('Good')">Good</span>
        <span :class="{'condition-active': active === 'Fair'}"
          @click="changeCondition('Fair')">Fair</span>
        <span :class="{'condition-active': active === 'Need Work'}"
          @click="changeCondition('Need Work')">Need Work</span>
        <span :class="{'condition-active': active === 'Tear Down'}"
          @click="changeCondition('Tear Down')">Tear Down</span>
      </div>
      <v-btn @click="onNext" class="select-view-button">Next</v-btn>
      <div class="skip-button" @click="onNext">
        <span>Skip</span>
      </div>
    </v-card-actions>
  </v-list>
</template>

<script>
export default {
  name: "GreatAlmostDoneComponent",
  props: ['onNext'],
  methods: {
    changeWalkout: function(choice) {
      console.log("-choice---changeWalkout--", choice);
      this.finished = choice;
    },
    changeFinished: function(choice) {
      console.log("-choice---changeFinished--", choice);
      this.finished = choice;
    },
    changeCondition: function(choice) {
      this.active = choice;
    }
  },
  data: () => ({
    finished: "no",
    walkout: "no",
    active: 'Good',
    age: 0
  })
};
</script>

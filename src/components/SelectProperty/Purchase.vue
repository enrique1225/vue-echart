<template>
  <v-list>
    <v-card-actions class="select-img-p purchase-section">
      <h2>When did you purchase your home?</h2>
      <div class="purchase-date">
        <v-img src="../../assets/calendar(1).svg" class="purchase-img"></v-img>
        <v-dialog ref="dialog" v-model="modal" :return-value.sync="date" persistent width="290px">
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="date"
              prepend-icon="event"
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-date-picker v-model="date" scrollable>
            <v-spacer></v-spacer>
            <v-btn text color="primary" @click="modal = false">Cancel</v-btn>
            <v-btn text color="primary" @click="$refs.dialog.save(date)">OK</v-btn>
          </v-date-picker>
        </v-dialog>
      </div>
      <v-btn @click="onNext" class="select-view-button">Done</v-btn>
    </v-card-actions>
  </v-list>
</template>

<script>
export default {
  name: "PurchaseComponent",
  props: ['onNext'],
  data: () => ({
    // date: new Date(),
    date: '2019-09-10',
    modal: false
  })
};
</script>

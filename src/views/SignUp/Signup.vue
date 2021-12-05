<template>
  <v-container class="form-container">
    <v-row>
      <v-col cols="4" class="left-signup items-centerall">
        <h3>sign up to:</h3>
        <p>
          <v-icon>library_add_check</v-icon>get monthly real estate reports
        </p>
        <p>
          <v-icon>library_add_check</v-icon>track the prices of your
          properties
        </p>
      </v-col>
      <v-col cols="8" class="right-signup signup-forms-call">
        <v-img src="../../assets/logo-img.png" class="logo-img"></v-img>

        <v-form v-model="valid">
          <v-row>
            <v-col cols="12" md="12" class="input-img">
              <v-img src="../../assets/user.svg" class="logo"></v-img>
              <v-text-field label="First name" solo></v-text-field>
            </v-col>
            <v-col cols="12" md="12" class="input-img">
              <v-img src="../../assets/user.svg" class="logo"></v-img>
              <v-text-field label="Last name" solo></v-text-field>
            </v-col>
            <v-col cols="12" md="12" class="input-img wa-input-email">
              <v-img src="../../assets/mail.svg" class="logo"></v-img>
              <v-text-field label="E-mail" solo></v-text-field>
            </v-col>
            <v-col cols="12" md="12" class="input-img">
              <v-img src="../../assets/lock.svg" class="logo"></v-img>
              <v-text-field label="Password" solo></v-text-field>
            </v-col>
            <v-col cols="12" md="12" class="input-img">
              <v-img src="../../assets/phone-call.svg" class="logo"></v-img>
              <v-text-field label="Phone" solo></v-text-field>
            </v-col>
            <v-col cols="12" md="12" class="terms-checkbox-s">
              <v-checkbox
                v-model="checkbox"
                :rules="[v => !!v || 'You must agree to continue!']"
                label="Accept terms and condition"
                required
              ></v-checkbox>
            </v-col>
            <v-col cols="12" md="12" class="input-img">
              <v-btn class="btn-default-all" text @click="submit">Sign Up</v-btn>
            </v-col>
            <v-col cols="12" md="12" class="input-img">
              <p>
                <router-link to="/login">Already user?</router-link>
              </p>
            </v-col>
          </v-row>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import router from "../../router";
export default {
  name: "Signup",
  methods: {
    submit: () => {
      router.push("portfolio");
    },
  },
  data: () => ({
    valid: false,
    checkbox: false,
  }),
  components: {},
};
</script>

<style scoped>
@import url("./signup.scss");
</style>

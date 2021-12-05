
<template>
  <v-container class="container">
    <v-row>
      <v-container class="form-container">
        <v-row>
          <v-col cols="12" class="right-signup">
            <v-img src="../../assets/logo-img.png" class="logo-img"></v-img>

            <v-form v-model="valid">
              <v-row>
                <v-col cols="12" md="12" class="input-img wa-input-email">
                  <v-img src="../../assets/mail.svg" class="logo"></v-img>
                  <v-text-field label="E-mail" solo></v-text-field>
                </v-col>
                <v-col cols="12" md="12" class="input-img">
                  <v-img src="../../assets/lock.svg" class="logo"></v-img>
                  <v-text-field label="Password" solo></v-text-field>
                </v-col>
                <v-col cols="12" md="12" class="input-img">
                  <v-btn class="btn-default-all" text @click="submit">Log In</v-btn>
                </v-col>
                <v-col cols="12" md="12" class="input-img">
                  <p>
                    <router-link to="/sign-up">New user?</router-link>
                  </p>
                </v-col>
              </v-row>
            </v-form>
          </v-col>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import router from "./../../router";

export default {
  name: "Login",
  methods: {
    submit: () => {
      // do login here.
      router.push("portfolio");
    },
  },
  data: () => ({
    valid: false,
  }),
};
</script>
<style scoped>
@import url("./login.scss");
</style>
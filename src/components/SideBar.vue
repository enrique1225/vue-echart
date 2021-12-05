<template>
  <v-col cols="1" class="portfolio-left-menu">
    <router-link to="/portfolio">
      <v-img src="./../assets/Praisal-Logo.svg" class="v-logo-main"></v-img>
    </router-link>
    <v-navigation-drawer permanent class-="main-header">
      <v-list class="profile-header">
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <router-link to="/profile">
              <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
            </router-link>
          </v-list-item-avatar>
        </v-list-item>
      </v-list>

      <v-list nav dense>
        <router-link to="/portfolio">
          <v-list-item link :class="{ 'menu-active': isActiveRoute('/portfolio') }">
            <v-list-item-icon>
              <v-img src="./../assets/home-icon.png" class="menu-imgs"></v-img>
              <v-img src="./../assets/home-active.png" class="menu-imgs"></v-img>
            </v-list-item-icon>
          </v-list-item>
        </router-link>
        <router-link to="/property">
          <v-list-item link :class="{ 'menu-active': isActiveRoute('/property') }">
            <v-list-item-icon>
              <v-img src="./../assets/menu-2.png" class="menu-imgs"></v-img>
              <v-img src="./../assets/menu-2-active.png" class="menu-imgs"></v-img>
            </v-list-item-icon>
          </v-list-item>
        </router-link>
        <router-link to="/portfolio">
          <v-list-item link>
            <v-list-item-icon>
              <v-img src="./../assets/menu-3.png" class="menu-imgs"></v-img>
              <v-img src="./../assets/menu-3-active.png" class="menu-imgs"></v-img>
            </v-list-item-icon>
          </v-list-item>
        </router-link>
        <router-link to="/portfolio">
          <v-list-item link>
            <v-list-item-icon>
              <v-img src="./../assets/menu-4.png" class="menu-imgs"></v-img>
              <v-img src="./../assets/menu-4-active.png" class="menu-imgs"></v-img>
            </v-list-item-icon>
          </v-list-item>
        </router-link>
      </v-list>
    </v-navigation-drawer>
  </v-col>
</template>

<script>
import router from './../router';

export default {
  name: "SideBarComponent",
  methods: {
    isActiveRoute: (url) => {
      return router && router.history.current.fullPath === url
    }
  },
};
</script>

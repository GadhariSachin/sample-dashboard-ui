<template>
  <div
    style="margin-top: 65px"
    @mouseover="showProfile = false"
    @mouseout="showProfile = true"
  >
    <v-navigation-drawer permanent expand-on-hover mini-variant.sync="mini">
      <v-list nav dense>
        <v-list-item>
          <v-list-item-avatar :class="{ 'profile--image': showProfile }">
            <v-img
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="John"
            ></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title> Welcome </v-list-item-title>
            <v-list-item-subtitle>John Adams</v-list-item-subtitle>
          </v-list-item-content></v-list-item
        >

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-view-grid</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Overview</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-google-analytics</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Analytics</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-car-hatchback</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Vehicles</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-car-wash</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Service</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-map</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Map</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-email</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Chat</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-wrench</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Settings</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "SidebarComponent",
  data() {
    return {
      showProfile: true,
    };
  },
};
</script>

<style scoped>
.profile--image {
  visibility: hidden;
}
</style>
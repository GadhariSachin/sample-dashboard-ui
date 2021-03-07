<template>
  <v-app-bar
    absolute
    color="white"
    elevate-on-scroll
    scroll-target="#scrolling-techniques-7"
  >
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-toolbar-title>velocity</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn icon>
      <v-badge
        bordered
        top
        color="deep-purple accent-4"
        dot
        offset-x="7"
        offset-y="10"
      >
        <v-icon>mdi-bell</v-icon>
      </v-badge>
    </v-btn>

    <v-btn icon
      ><v-badge
        bordered
        top
        color="deep-purple accent-4"
        dot
        offset-x="5"
        offset-y="8"
      >
        <v-icon>mdi-email</v-icon>
      </v-badge>
    </v-btn>

    <v-btn icon>
      <v-avatar style="height: 30px; width: auto">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "NavbarComponent",
};
</script>

<style scoped>
.navbar--wrapper {
  outline: 1px solid;
}
</style>
<template>
  <div class="top--drivers--container">
    <v-card>
      <v-card-title primary-title class="card--heading">
        TOP DRIVERS
      </v-card-title>
      <v-card-text>
        <v-list subheader>
          <v-list-item v-for="driver in recent" :key="driver.title">
            <v-list-item-avatar>
              <v-img
                :alt="`${driver.title} avatar`"
                :src="driver.avatar"
              ></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title v-text="driver.name"></v-list-item-title>
              <v-list-item-subtitle v-text="driver.car"></v-list-item-subtitle>
            </v-list-item-content>

            <v-spacer></v-spacer>

            <v-list-item-content>
              <v-list-item-title> $ {{ driver.earning }}</v-list-item-title>
              <v-list-item-subtitle
                v-text="driver.distance"
              ></v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "TopDriversComponent",
  data() {
    return {
      recent: [
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
          name: "Jason Oner",
          car: "Tesla Model X",
          earning: 123,
          distance: 4000,
        },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
          name: "Mike Carlson",
          car: "BMW M3",
          earning: 123,
          distance: 4000,
        },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
          name: "Cindy Baker",
          car: "Tesla Model X",
          earning: 123,
          distance: 4000,
        },
      ],
    };
  },
};
</script>

<style scoped>
.top--drivers--container {
  height: 300px;
  padding: 30px;
}
.card--heading {
  font-size: 14px;
  color: lightgray;
}
</style>
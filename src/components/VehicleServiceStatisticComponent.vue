<template>
  <div class="service--stats--container">
    <v-card>
      <v-card-title primary-title class="card--heading">
        VEHICLE SERVICE STATUS
      </v-card-title>
      <v-card-text style="height: 200px">
        <pie-chart
          :data="[
            ['Blueberry', 44],
            ['Strawberry', 23],
          ]"
          :donut="true"
        ></pie-chart>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "VehicleServiceStatisticComponent",
};
</script>

<style scoped>
.service--stats--container {
  height: 300px;
  padding: 30px;
}
.card--heading {
  font-size: 14px;
  color: lightgray;
}
</style>
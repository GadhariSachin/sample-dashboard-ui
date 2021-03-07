<template>
  <div class="service--center--container">
    <v-card>
      <v-card-title primary-title class="card--heading">
        SERVICE CENTERS
      </v-card-title>
      <v-card-text style="height: 510px"> </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "ServiceCentersComponent",
};
</script>

<style scoped>
.service--center--container {
  height: 600px;
  padding: 30px;
}
.card--heading {
  font-size: 14px;
  color: lightgray;
}
</style>
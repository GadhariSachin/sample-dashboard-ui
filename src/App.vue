<template>
  <v-app>
    <Navbar />
    <v-main>
      <div class="d-flex">
        <Sidebar />
        <div class="dashboard--wrapper">
          <div class="dashboard--reminderboard--container">
            <ServicesBoard />
          </div>
          <div class="dashboard--heading">
            <p class="heading--background">EXPAND BOARDS</p>
          </div>
          <hr style="margin-top: -28px; margin-bottom: 20px" />
          <div class="dashboard--services--container">
            <div class="dashboard--servicecenters">
              <ServiceCenters />
            </div>
            <div class="dashboard--services--stats">
              <VehicleServiceStatistic />
              <TopDrivers />
            </div>
          </div>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {
    Navbar: () => import("@/components/NavbarComponent.vue"),
    Sidebar: () => import("@/components/SidebarComponent.vue"),
    ServiceCenters: () => import("@/components/ServiceCentersComponent.vue"),
    ServicesBoard: () => import("@/components/ServicesBoardComponent.vue"),
    TopDrivers: () => import("@/components/TopDriversComponent.vue"),
    VehicleServiceStatistic: () =>
      import("@/components/VehicleServiceStatisticComponent.vue"),
  },

  data: () => ({
    //
  }),
};
</script>


<style scoped>
.dashboard--wrapper {
  background-color: #f4f6fc;
  width: 100%;
  box-sizing: border-box;
  margin-top: 65px;
}
.dashboard--reminderboard--container {
  height: auto;
  padding: 20px;
  margin-bottom: 20px;
}
.dashboard--services--container {
  height: auto;
  display: flex;
  width: 100%;
  padding: 20px;
  margin-top: 30px;
}
.dashboard--servicecenters {
  outline: 1px solid;
  flex: 0.6;
}
.dashboard--services--stats {
  flex: 0.4;
}
.dashboard--heading {
  display: flex;
  justify-content: center;
  margin: 0px 20px;
}
.heading--background {
  background-color: #f4f6fc;
  padding: 0px 10px;
  font-size: 14px;
  letter-spacing: 1px;
  font-weight: 500;
  color: lightgray;
}
hr {
  margin-top: -28px;
  margin-bottom: 20px;
  margin-right: 20px;
  margin-left: 20px;
}
</style>
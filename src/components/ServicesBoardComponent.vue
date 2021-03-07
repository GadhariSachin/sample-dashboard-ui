<template>
  <div class="sidebar--wrapper">
    <p class="sidebar--title">Service Reminders</p>
    <div class="row">
      <div class="col-3 service--board">
        <h6>
          SERVICE NEEDED
          <v-chip
            class="ma-2"
            color="blue lighten-3"
            x-small
            text-color="indigo"
          >
            76
          </v-chip>
        </h6>
        <draggable class="list-group" :list="list1" group="people">
          <v-card
            class="canban--card"
            v-for="element in list1"
            :key="element.id"
          >
            <div class="card--body">
              <div>
                <h6>{{ element.name }}</h6>
                <p>{{ element.task }}</p>
              </div>
              <div>
                <h6>$ {{ element.cost }}</h6>
                <p>{{ element.date }}</p>
              </div>
            </div>
          </v-card>
        </draggable>
      </div>

      <div class="col-3 waiting--board">
        <h6>
          WAITING
          <v-chip
            class="ma-2"
            color="deep-purple lighten-3"
            x-small
            text-color="deep-purple"
          >
            69
          </v-chip>
        </h6>
        <draggable class="list-group" :list="list2" group="people">
          <v-card
            class="canban--card"
            v-for="element in list2"
            :key="element.id"
          >
            <div class="card--body">
              <div>
                <h6>{{ element.name }}</h6>
                <p>{{ element.task }}</p>
              </div>
              <div>
                <h6>$ {{ element.cost }}</h6>
                <p>{{ element.date }}</p>
              </div>
            </div>
          </v-card>
        </draggable>
      </div>
      <div class="col-3 inservice--board">
        <h6>
          IN SERVICE
          <v-chip
            class="ma-2"
            color="cyan accent-2"
            x-small
            text-color="cyan darken-3"
          >
            28
          </v-chip>
        </h6>
        <draggable class="list-group" :list="list3" group="people">
          <v-card
            class="canban--card"
            v-for="element in list3"
            :key="element.id"
          >
            <div class="card--body">
              <div>
                <h6>{{ element.name }}</h6>
                <p>{{ element.task }}</p>
              </div>
              <div>
                <h6>$ {{ element.cost }}</h6>
                <p>{{ element.date }}</p>
              </div>
            </div>
          </v-card>
        </draggable>
      </div>
      <div class="col-3 fully--serviced--board">
        <h6>
          FULLY SERVICED
          <v-chip
            class="ma-2"
            color="yellow lighten-3"
            x-small
            text-color="yellow darken-2"
          >
            198
          </v-chip>
        </h6>
        <draggable class="list-group" :list="list4" group="people">
          <v-card
            class="canban--card"
            v-for="element in list4"
            :key="element.id"
          >
            <div class="card--body">
              <div>
                <h6>{{ element.name }}</h6>
                <p>{{ element.task }}</p>
              </div>
              <div>
                <h6>$ {{ element.cost }}</h6>
                <p>{{ element.date }}</p>
              </div>
            </div>
          </v-card>
        </draggable>
      </div>
    </div>
  </div>
</template>

<script>
import draggable from "vuedraggable";

export default {
  name: "ServiceBoardComponent",

  data() {
    return {
      list1: [
        {
          id: "i11",
          name: "Spire",
          cost: 433,
          task: "Tire Replacement",
          date: "June 12",
        },
        {
          id: "i1121",
          name: "EOS",
          cost: 120,
          task: "Engine check up",
          date: "May 12",
        },
        {
          id: "i9876",
          name: "Eagle",
          cost: 34,
          task: "Tire Replacement",
          date: "June 6",
        },
        {
          id: "i11988",
          name: "Spire",
          cost: 43,
          task: "Monthly Service",
          date: "June 12",
        },
      ],
      list2: [
        {
          id: "w2380",
          name: "Expedition",
          cost: 433,
          task: "Tire Replacement",
          date: "June 12",
        },
        {
          id: "w2432",
          name: "PIRE",
          cost: 120,
          task: "Engine check up",
          date: "May 12",
        },
        {
          id: "w54",
          name: "Mani",
          cost: 34,
          task: "Tire Replacement",
          date: "June 6",
        },
      ],
      list3: [
        {
          id: "t3r2",
          name: "Scorpion",
          cost: 67,
          task: "Tire Replacement",
          date: "June 12",
        },
        {
          id: "i1121",
          name: "Testt",
          cost: 120,
          task: "Engine check up",
          date: "May 12",
        },
      ],
      list4: [
        {
          id: "y11",
          name: "Spire",
          cost: 433,
          task: "Tire Replacement",
          date: "June 12",
        },
        {
          id: "y1121",
          name: "EOS",
          cost: 120,
          task: "Engine check up",
          date: "May 12",
        },
        {
          id: "y9876",
          name: "Eagle",
          cost: 34,
          task: "Tire Replacement",
          date: "June 6",
        },
        {
          id: "y11988",
          name: "Spire",
          cost: 43,
          task: "Monthly Service",
          date: "June 12",
        },
      ],
    };
  },

  components: {
    draggable,
  },
};
</script>

<style scoped>
.sidebar--wrapper {
  height: 100%;
}
.sidebar--title {
  font-size: 24px;
  font-weight: 200;
}
.card--body {
  display: flex;
  justify-content: space-between;
  padding: 5px 10px;
}
.canban--card {
  margin-bottom: 10px;
}
.service--board .canban--card {
  border-left: 3px solid blue;
}
.waiting--board .canban--card {
  border-left: 3px solid indigo;
}
.inservice--board .canban--card {
  border-left: 3px solid cyan;
}
.fully--serviced--board .canban--card {
  border-left: 3px solid orange;
}
</style>
<template>
  <nav>
    <v-navigation-drawer
      v-model="drawer"
      dark
      app
      mini-variant
      class="deep-purple lighten-2"
    >
      <v-list tile>
        <v-list-item class="mb-8" router to="/">
          <v-list-item-action>
            <v-icon>fas fa-window-restore</v-icon>
          </v-list-item-action>
        </v-list-item>
        <v-list-item class="mb-8">
          <v-list-item-action>
            <v-icon>far fa-clock</v-icon>
          </v-list-item-action>
        </v-list-item>
        <v-list-item class="mb-8">
          <v-list-item-action>
            <v-icon>fas fa-chart-line</v-icon>
          </v-list-item-action>
        </v-list-item>
        <v-list-item class="mb-8">
          <v-list-item-action>
            <v-icon>far fa-comment-alt</v-icon>
          </v-list-item-action>
        </v-list-item>
        <v-list-item class="mb-8">
          <v-list-item-action>
            <v-icon>fas fa-cog</v-icon>
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <GChart type="ColumnChart" :data="chartData" :options="chartOptions" />
    <v-navigation-drawer
      v-model="right"
      dark
      app
      class="deep-purple lighten-3"
      fixed
      right
    >
      <v-layout column align-center>
        <v-flex class="mt-5">
          <v-avatar size="100">
            <img src="../assets/green.jpg" alt="" />
          </v-avatar>
          <h4 class="white--text subheading mt-1 text-center">Julian Neal</h4>
          <h6 class="white--text subheading mt-1 text-center">
            CEO.Almz Pvt.Ltd
          </h6>
        </v-flex>
      </v-layout>
      <p class="white--text subheading pl-3 mt-3">Rank of Company</p>
      <v-list rounded dense>
        <v-list-item router to="/">
          <v-list-item-action> 03 </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>The Income</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router to="/">
          <v-list-item-action> 05 </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Human Resources</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router to="/">
          <v-list-item-action> 12 </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>The Growth</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <p class="white--text subheading pl-3 mt-3">Next Meeting Places</p>
      <v-timeline align-top dense fill-dot small dark>
        <v-timeline-item fill-dot small color="white" class="white--text"
          >Norisseeberg</v-timeline-item
        >
        <v-timeline-item fill-dot small color="white" class="white--text"
          >East Mortanstad</v-timeline-item
        >
        <v-timeline-item fill-dot small color="white" class="white--text"
          >Andersonland</v-timeline-item
        >
      </v-timeline>
    </v-navigation-drawer>
  </nav>
</template>

<script>
import { GChart } from "vue-google-charts";
const gradients = [
  ["#222"],
  ["#42b3f4"],
  ["red", "orange", "yellow"],
  ["purple", "violet"],
  ["#00c6ff", "#F0F", "#FF0"],
  ["#f72047", "#ffd200", "#1feaea"],
];
export default {
  components: {
    GChart,
  },
  data() {
    return {
      picker: new Date.toISOString().substr(0, 10),
      chartData: [
      
      ],
      chartOptions: {
        chart: {
          title: "Company Performance",
          subtitle: "Sales, Expenses, and Profit: 2014-2017",
        },
      },
      showLabels: false,
      lineWidth: 2,
      labelSize: 7,
      radius: 10,
      padding: 8,
      lineCap: "round",
      gradient: gradients[5],
      value: [2, 2, 5, 9, 5, 10, 3, 5, -4, -10, 1, 8, 2, 9, 0],
      geadientDirection: "top",
      gradients,
      fill: false,
      type: "trend",
      autoLineWidth: false,
    };
  },
};
</script>

<style>
</style>
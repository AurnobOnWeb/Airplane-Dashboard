<template>
  <BubbleChart :data="chartData" :options="chartOptions" />
</template>

<script>
import {
  Chart as ChartJS,
  Tooltip,
  Legend,
  PointElement,
  LinearScale,
  ScatterController, // Add ScatterController for Bubble Chart
  CategoryScale, // Add CategoryScale for Bubble Chart
} from "chart.js";
import { Bubble } from "vue-chartjs";

ChartJS.register(
  LinearScale,
  PointElement,
  Tooltip,
  Legend,
  ScatterController,
  CategoryScale
);

export default {
  data() {
    return {
      chartData: {
        datasets: [
          {
            label: "VueJS",
            backgroundColor: "#f87979",
            data: [
              {
                x: 20,
                y: 25,
                r: 5,
              },
              {
                x: 40,
                y: 10,
                r: 10,
              },
              {
                x: 30,
                y: 22,
                r: 30,
              },
            ],
          },
          {
            label: "React",
            backgroundColor: "#7C8CF8",
            data: [
              {
                x: 10,
                y: 30,
                r: 15,
              },
              {
                x: 20,
                y: 20,
                r: 10,
              },
              {
                x: 15,
                y: 8,
                r: 30,
              },
            ],
          },
        ],
      },
      chartOptions: {
        responsive: true,
      },
    };
  },
  components: {
    BubbleChart: Bubble,
  },
};
</script>

<template>
  <DoughnutChart :data="chartData" :options="chartOptions" />
</template>

<script>
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from "chart.js";
import { Doughnut } from "vue-chartjs";
ChartJS.register(ArcElement, Tooltip, Legend);
export default {
  data() {
    return {
      chartData: {
        labels: ["VueJS", "emberJs", "reactJs", "angularJs"],
        datasets: [
          {
            backgroundColor: ["#41B883", "#E46651", "#00D8FF", "#DD1816"],
            data: [40, 20, 70, 10],
          },
        ],
      },
      chartOptions: {
        responsive: true,
      },
    };
  },
  components: {
    DoughnutChart: Doughnut,
  },
};
</script>

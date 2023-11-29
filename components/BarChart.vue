<template>
  <Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
</template>

<script>
import { Bar } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale,
} from "chart.js";

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale
);

export default {
  name: "BarChart",
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: [
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
          "Jan 2022 - 2024",
        ],
        datasets: [
          {
            label: "Personal Services",
            backgroundColor: "#1D1D1D",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Supplies & Equipment",
            backgroundColor: "rgba(29, 29, 29, 0.8)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Capital Outlay",
            backgroundColor: "rgba(29, 29, 29, 0.6)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Indirect Cost Allocation",
            backgroundColor: "rgba(29, 29, 29, 0.5)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Other Charges",
            backgroundColor: "rgba(29, 29, 29, 0.4)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Services & Charges",
            backgroundColor: "rgba(29, 29, 29, 0.3)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Transfers Out",
            backgroundColor: "rgba(29, 29, 29, 0.2)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
          {
            label: "Expanses",
            backgroundColor: "rgba(29, 29, 29, 0.1)",
            data: [5, 10, 15, 20, 25, 30, 35],
          },
        ],
      },
      chartOptions: {
        plugins: {
          title: {
            display: false,
            text: "Chart.js Bar Chart - Stacked",
          },
          legend: {
            // display: true,
            position: "right",
          },
        },
        responsive: true,
        scales: {
          x: {
            stacked: true,
          },
          y: {
            stacked: true,
          },
        },
      },
    };
  },
};
</script>

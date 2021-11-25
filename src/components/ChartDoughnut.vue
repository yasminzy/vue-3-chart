<template>
  <DoughnutChart
    :chart-data="data"
    :options="options"
    css-classes="chart-container"
  />
</template>

<script setup>
import pattern from "patternomaly"
import { ref, computed } from "vue"
import { DoughnutChart } from "vue-chart-3"
import { Chart, DoughnutController, ArcElement } from "chart.js"

Chart.register(DoughnutController, ArcElement)

const dataValues = ref([10, 20, 40])

const data = computed(() => ({
  labels: ["Foo", "Bar", "Baz"],

  datasets: [
    {
      data: dataValues.value,
      backgroundColor: pattern.generate(["#859900", "#d33682", "#cb4b16"])
    }
  ]
}))

const options = ref({
  plugins: {
    title: {
      text: "Doughnut"
    }
  }
})
</script>

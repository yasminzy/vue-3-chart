<template>
  <div class="container">
    <ChartBar />
    <ChartDoughnut />
    <ChartLine />
  </div>
</template>

<script setup>
import ChartBar from "./components/ChartBar.vue"
import ChartDoughnut from "./components/ChartDoughnut.vue"
import ChartLine from "./components/ChartLine.vue"
</script>

<style>
body {
  background-color: #fdf6e3;
  min-height: 100vh;
  color: #657b83;
  width: 100%;
  padding: 2rem;
}

.container {
  margin: 0 auto;
  width: 91.666667%;
  display: grid;
  gap: 2rem;
}

@media (min-width: 1024px) {
  .container {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}

.chart-container {
  background-color: #eee8d5;
  border-radius: 0.5rem;
}
</style>

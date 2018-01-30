<template>
  <section>
    <h2>Motivation Tracker</h2>
    <div ref="chart" />
  </section>
</template>

<script>
import Tauchart, { Chart } from 'taucharts'
import 'taucharts/build/production/tauCharts.default.min.css'
import 'taucharts/build/development/plugins/tauCharts.tooltip.js'
import 'taucharts/build/development/plugins/tauCharts.tooltip.css'

function sendRequest() {
  return new Promise(resolve => {
    const xhr = new XMLHttpRequest()
    xhr.open('GET', 'https://script.google.com/macros/s/AKfycbz0ZAT-X7UctEiwTEsnTqRwqBOnjeX6SRA3Ob0tI-XBamx89Ms/exec')
    xhr.onreadystatechange = () => {
      if (xhr.readyState === 4 && (xhr.status === 200 || xhr.status === 304)) {
        resolve(xhr.response)
      }
    }
    xhr.responseType = 'json'
    xhr.send(null)
  })
}
function processData(data) {
  const newData = []
  for (let datum of data) {
    newData.push({ title: 'keydowns', date: datum.date, count: datum.keydowns })
    newData.push({ title: 'clicks', date: datum.date, count: datum.clicks })
  }
  return newData
}

export default {
  mounted() {
    sendRequest().then(data => {
      this.drawChart(processData(data))
    })
  },
  methods: {
    drawChart(data) {
      const chart = new Chart({
        type: 'stacked-area',
        x: 'date',
        y: 'count',
        color: 'title',
        data,
        plugins: [
          Tauchart.api.plugins.get('tooltip')()
        ]
      })
      chart.renderTo(this.$refs.chart)
    }
  }
}
</script>

<style scoped>
section {
  height: 300px;
}
h2 {
  margin: 0 0 0 30px;
  height: 100px;
}
div {
  height: 200px;
}
</style>

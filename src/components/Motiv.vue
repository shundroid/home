<template lang="pug">
section
  .chart(ref="chart")
  .details
    | Today I had
    .num.keydowns {{ keydowns }}
    | keypresses and
    .num.clicks {{ clicks }}
    | clicks.
</template>

<script>
import Tauchart, { Chart } from 'taucharts'
import 'taucharts/dist/taucharts.min.js'
import 'taucharts/dist/taucharts.min.css'
import 'taucharts/dist/plugins/tooltip.js'
import 'taucharts/dist/plugins/tooltip.css'

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
  data() {
    return {
      motiv: null
    }
  },
  mounted() {
    sendRequest().then(data => {
      this.motiv = data;
    })
  },
  watch: {
    motiv() {
      if (!this.motiv) return
      const chart = new Chart({
        type: 'line',
        x: 'date',
        y: 'count',
        color: 'title',
        data: processData(this.motiv),
        plugins: [
          Tauchart.api.plugins.get('tooltip')()
        ],
        guide: {
          color: {
            brewer: {
              keydowns: '#E91E63',
              clicks: '#00C853'
            }
          }
        }
      })
      chart.renderTo(this.$refs.chart)
    }
  },
  computed: {
    keydowns() {
      // eslint-disable-next-line no-console
      return this.motiv ? this.motiv[this.motiv.length - 1].keydowns : '----'
    },
    clicks() {
      return this.motiv ? this.motiv[this.motiv.length - 1].clicks : '---'
    }
  }
}
</script>

<style scoped>
section {
  height: 200px;
  display: flex;
  justify-content: flex-end;
}
.chart {
  height: 100%;
  flex: 1;
}
.details {
  font-family: 'Electrolize', serif;
  text-align: center;
  margin: 0 60px;
  font-size: 1.3em;
}
.num {
  font-size: 1.5em;
}
.keydowns {
  color: #E91E63;
}
.clicks {
  color: #00C853;
}
</style>

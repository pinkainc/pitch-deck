<template>
  <div class="chart-container">
    <canvas v-if="type === 'line' || type === 'bar'" ref="chartCanvas"></canvas>
    <div v-else ref="d3Container"></div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { Chart } from 'chart.js/auto'
import * as d3 from 'd3'

const props = defineProps({
  data: Object,
  type: {
    type: String,
    default: 'line'
  },
  title: String
})

const chartCanvas = ref(null)
const d3Container = ref(null)

onMounted(() => {
  if (props.type === 'line' || props.type === 'bar') {
    // Chart.js for simple charts
    new Chart(chartCanvas.value, {
      type: props.type,
      data: {
        labels: props.data.labels,
        datasets: [{
          label: props.title,
          data: props.data.values,
          borderColor: '#000',
          backgroundColor: props.type === 'bar' ? '#000' : 'transparent',
          tension: 0.4
        }]
      },
      options: {
        responsive: true,
        plugins: {
          legend: { display: false },
          title: {
            display: !!props.title,
            text: props.title
          }
        },
        scales: {
          y: {
            beginAtZero: true,
            grid: {
              color: '#e4e4e7'
            }
          },
          x: {
            grid: {
              display: false
            }
          }
        }
      }
    })
  } else if (props.type === 'tam') {
    // D3.js for TAM/SAM/SOM circles
    const width = 400
    const height = 400
    
    const svg = d3.select(d3Container.value)
      .append('svg')
      .attr('width', width)
      .attr('height', height)
    
    const circles = [
      { radius: 180, label: 'TAM', value: props.data.tam },
      { radius: 120, label: 'SAM', value: props.data.sam },
      { radius: 60, label: 'SOM', value: props.data.som }
    ]
    
    const g = svg.append('g')
      .attr('transform', `translate(${width/2}, ${height/2})`)
    
    circles.forEach((circle, i) => {
      g.append('circle')
        .attr('r', circle.radius)
        .attr('fill', 'none')
        .attr('stroke', '#000')
        .attr('stroke-width', 2)
        .attr('opacity', 0.3 + i * 0.2)
      
      g.append('text')
        .attr('y', -circle.radius + 20)
        .attr('text-anchor', 'middle')
        .style('font-weight', 'bold')
        .text(`${circle.label}: ${circle.value}`)
    })
  }
})
</script>
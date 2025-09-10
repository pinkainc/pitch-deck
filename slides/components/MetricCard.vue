<template>
  <div class="metric-card">
    <div class="metric-value">{{ formattedValue }}</div>
    <div class="metric-label">{{ label }}</div>
    <div v-if="change" class="metric-change">
      {{ change > 0 ? '+' : '' }}{{ change }}%
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  value: [Number, String],
  label: String,
  change: Number,
  format: {
    type: String,
    default: 'number'
  }
})

const formattedValue = computed(() => {
  if (props.format === 'currency') {
    return `€${props.value.toLocaleString()}`
  } else if (props.format === 'percentage') {
    return `${props.value}%`
  } else {
    return props.value.toLocaleString()
  }
})
</script>
<script setup>
import { defineEmits, defineProps } from 'vue'
const emit = defineEmits(['change-event'])
const props = defineProps({
  dotValue: Number,
})
const changeValue = (val) => {
  emit('change-event', val)
}
</script>
<style lang="scss">
.dot {
  cursor: pointer;
}
</style>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" role="buttons" width="100%" height="100">
    <line x1="2" y1="50" x2="99%" y2="50" style="stroke: #a98f78; stroke-width: 2" />
    <line x1="95%" y1="40" x2="99%" y2="50" style="stroke: #a98f78; stroke-width: 2" />
    <line x1="95%" y1="60" x2="99%" y2="50" style="stroke: #a98f78; stroke-width: 2" />
    <circle r="1" cx="2" cy="50" fill="#a98f78" />
    <circle r="1" cx="99%" cy="50" fill="#a98f78" />
    <circle r="1" cx="95%" cy="40" fill="#a98f78" />
    <circle r="1" cx="95%" cy="60" fill="#a98f78" />
    <text x="5" y="75" fill="#a1dddd" font-size="12">2024</text>
    <text x="80%" y="75" fill="#a1dddd" font-size="12">2025</text>
    <!-- btn -->
    <circle
      class="dot"
      r="10"
      cx="25%"
      cy="50"
      :fill="dotValue === 0 ? '#a1dddd' : '#6b9696'"
      stroke="#a98f78"
      stroke-width="3"
      @click="changeValue(0)"
    />
    <circle
      class="dot"
      r="10"
      cx="40%"
      cy="50"
      :fill="dotValue === 1 ? '#a1dddd' : '#6b9696'"
      stroke="#a98f78"
      stroke-width="3"
      @click="changeValue(1)"
    />
    <circle
      class="dot"
      r="10"
      cx="55%"
      cy="50"
      :fill="dotValue === 2 ? '#a1dddd' : '#6b9696'"
      stroke="#a98f78"
      stroke-width="3"
      @click="changeValue(2)"
    />
  </svg>
</template>

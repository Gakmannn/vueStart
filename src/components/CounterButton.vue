<script setup lang="ts">
import { ref } from 'vue'
const props = defineProps(['start'])
const start = props.start ? props.start : 0
const counter = ref(start)
</script>

<template>
  <button @click="counter++">{{ counter }}</button>
</template>

<style scoped></style>

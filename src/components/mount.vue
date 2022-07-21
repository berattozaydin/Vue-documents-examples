<script setup>
import { useMouse } from './returnmout.vue'

const { x, y } = useMouse()
</script>

<template>Mouse position is at: {{ x }}, {{ y }}</template>
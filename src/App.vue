<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'

const handleClick = (...args: any[]) => {
  console.log(...args)
}
</script>

<template>
  <HelloWorld @click="handleClick" />
</template>

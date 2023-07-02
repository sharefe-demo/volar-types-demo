<script setup lang="ts">

import type { ObjectEmitsOptions } from 'vue'

interface EmitsOptions extends /* @vue-ignore */ ObjectEmitsOptions {
  (event: 'click', data: string): void
}

const emit = defineEmits<EmitsOptions>()

const handleClick = () => {
  emit('click', 'You have clicked me!')
}
</script>

<template>
  <div :style="{ textAlign: 'center' }">
    <h3>Hello World</h3>
    <div style="cursor: pointer; color: red;" @click="handleClick">click me</div>
  </div>
</template>

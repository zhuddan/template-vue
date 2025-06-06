<script setup lang="ts">
import { useAppStore } from '~/store/app'

defineOptions({
  name: 'IndexPage',
})
const store = useAppStore()
</script>

<template>
  <h1>My project template </h1>
  <div class="m-2 flex justify-center gap-2">
    <button
      class="icon-btn" @click="store.reduce"
    >
      <div class="i-carbon:arrow-left" />
    </button>
    {{ store.$state.count }}
    <button
      class="icon-btn" @click="store.increase"
    >
      <div class="i-carbon:arrow-right" />
    </button>
  </div>
</template>

<route lang="yaml">
  meta:
    layout: home
    bgColor: yellow
</route>

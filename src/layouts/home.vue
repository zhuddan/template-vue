<script setup lang="ts">
import { useAppStore } from '~/store/app'

const { count } = toRefs(useAppStore())
</script>

<template>
  <main
    class="px-4 py-10 text-center text-dark:gray-200 text-gray-700"
  >
    <RouterView />
    <TheFooter />
    <div class="mx-auto mt-5 text-center text-sm opacity-50">
      [Home Layout count is {{ count }}]
    </div>
  </main>
</template>

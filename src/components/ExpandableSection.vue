<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
})

const isOpen = ref(false)
</script>

<template>
  <div class="">
    <button class="w-full rounded-lg p-4 text-left hover:bg-gray-100" @click="isOpen = !isOpen">
      <div class="flex items-center gap-3">
        <i :class="isOpen ? 'pi pi-chevron-up' : 'pi pi-chevron-down'" text-xs />

        <span>{{ props.title }}</span>
      </div>
    </button>
    <div v-if="isOpen" class="bg-white p-4">
      <slot />
    </div>
  </div>
</template>

<style scoped>
/* No additional styles needed as Tailwind CSS is used */
</style>

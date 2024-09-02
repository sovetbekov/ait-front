<script setup lang="ts">
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  type: {
    type: String,
    required: true,
  },
  duration: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="">
    <button class="w-full rounded-lg px-3 py-1 text-left" @click="isOpen = !isOpen">
      <div class="flex flex-row items-center gap-3">
        <div class="module-name flex flex-row items-center gap-2">
          <i class="pi pi-file" /> <!-- based on type illustrate diff icons -->
          <span>{{ props.title }}</span>
        </div>
        <span>{{ props.duration }}</span>
      </div>
    </button>
  </div>
</template>

<style scoped>
/* No additional styles needed as Tailwind CSS is used */
</style>

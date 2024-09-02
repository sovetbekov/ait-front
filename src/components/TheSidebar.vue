<script setup lang="ts">
import 'primeicons/primeicons.css'

const { t } = useI18n()
const router = useRouter()
</script>

<template>
  <div class="flex flex-col justify-between text-left" min-h-screen>
    <div class="flex flex-grow flex-col gap-2">
      <RouterLink to="/" :title="t('button.home')" mb-6 icon-btn>
        <img src="/ait-old-logo.png" width="100">
      </RouterLink>
      <div class="items">
        <div class="mb-1 flex cursor-pointer items-center rounded-lg bg-white p-4 hover:bg-gray-200" @click="router.push('/')">
          <i class="pi pi-home mr-3" />
          {{ t('sidebar.main') }}
        </div>
        <div class="mb-1 flex cursor-pointer items-center rounded-lg bg-white p-4 hover:bg-gray-200" @click="router.push('/courses')">
          <i class="pi pi-book mr-3" />
          {{ t('sidebar.courses') }}
        </div>
        <div class="mb-1 flex cursor-pointer items-center rounded-lg bg-white p-4 hover:bg-gray-200">
          <i class="pi pi-list mr-3" />
          {{ t('sidebar.exams') }}
        </div>
        <div class="mb-1 flex cursor-pointer items-center rounded-lg bg-white p-4 hover:bg-gray-200">
          <i class="pi pi-heart mr-3" />
          {{ t('sidebar.favs') }}
        </div>
      </div>
    </div>

    <div class="profile mt-auto flex flex-row items-center">
      <img src="/ait-old-logo.png" width="50" class="mr-2">
      Dastan Sembekov
    </div>
  </div>
</template>

<style scoped>
/* No additional styles needed as Tailwind CSS is used */
</style>

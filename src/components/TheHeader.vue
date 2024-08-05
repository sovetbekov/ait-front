<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div flex="~ gap-2 " mx-auto mt-6 items-center justify-between>
    <div class="flex flex-row items-center gap-22">
      <RouterLink to="/" :title="t('button.home')" icon-btn>
        <img src="../../public/logo.png" width="100">
      </RouterLink>

      <div flex="~ gap-10" text-normal>
        <RouterLink icon-btn to="/contacts" :title="t('header.contacts')" data-test-id="contacts">
          {{ t('header.contacts') }}
        </RouterLink>
        <RouterLink icon-btn to="/about" :title="t('header.about')" data-test-id="about">
          {{ t('header.about') }}
        </RouterLink>
        <RouterLink icon-btn to="/courses" :title="t('header.courses')" data-test-id="courses">
          {{ t('header.courses') }}
        </RouterLink>
      <!-- <button icon-btn :title="t('button.toggle_dark')" @click="toggleDark()">
        <div i="carbon-sun dark:carbon-moon" />
      </button> -->
      </div>
    </div>

    <div class="flex flex-row items-center gap-4">
      <button class="button-6" rounded-lg>
        {{ t('header.login') }}
      </button>
      <button class="button-31" rounded-lg>
        {{ t('header.create-account') }}
      </button>
    </div>
  </div>
</template>

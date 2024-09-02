<script setup lang="ts">
const { t } = useI18n()
const username = ref('')
const password = ref('')

function handleLogin() {
  // Handle login logic here
  // console.log('Username:', username.value)
  // console.log('Password:', password.value)
}
</script>

<template>
  <main
    py-20
    text="center gray-700 dark:gray-200"
  >
    <div class="flex flex-col items-center gap-10">
      <RouterLink to="/" :title="t('button.home')" icon-btn>
        <img src="/ait-old-logo.png" width="100">
      </RouterLink>
      <p class="text-4xl font-semibold">
        Создать аккаунт
      </p>

      <form class="max-w-xs w-full flex flex-col items-center gap-3 rounded-lg" @submit.prevent="handleLogin">
        <div class="input-group">
          <label for="username" font-medium>{{ t('login.username') }}</label>
          <input
            id="username"
            v-model="username"
            type="text"
            class="input-field"
            required
          >
        </div>
        <div class="input-group">
          <label for="password" font-medium>{{ t('login.password') }}</label>
          <input
            id="password"
            v-model="password"
            type="password"
            class="input-field"
            required
          >
        </div>
        <div class="flex flex-row gap-4">
          <button type="submit" class="button-6" rounded-lg>
            {{ t('login.create') }}
          </button>
        </div>
      </form>
      <RouterLink to="/signin/create-account" :title="t('login.registration')" icon-btn>
        <div class="gap-2 text-sm">
          <span class="text-[#ced4da]">{{ t('login.already-acc') }}</span> <span class="text-[#0d1b2a]">{{ t('login.login') }}</span>
        </div>
      </RouterLink>
    </div>
  </main>
</template>

<style scoped>
.input-field {
  padding: 10px;
  width: 100%;
  border: 1px solid #ccc;
  border-radius: 14px;
  margin-bottom: 10px;
}

.input-group {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-bottom: 10px;
}

.input-group label {
  margin-bottom: 5px;
}
</style>

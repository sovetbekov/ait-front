<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
})
const { t } = useI18n()
</script>

<template>
  <div class="my-20 min-h-screen flex flex-col gap-40 text-[#021f15]">
    <div class="relative flex flex-col gap-6 rounded-md bg-[#f0f5ef] px-6 py-10 shadow lg:px-40 md:px-20 md:py-20 xl:px-60">
      <div class="mx-auto flex flex-col gap-5 text-3xl font-bold lg:text-5xl md:text-4xl">
        <span>
          {{ t('title.hook') }}
        </span>
        <span class="mx-auto border-2 border-[#5de064] rounded-md object-cover p-1">
          {{ t('title.hook2') }}
        </span>
      </div>

      <div>
        {{ t('title.description') }}
      </div>
      <div class="relative mt-8">
        <img class="z-10 w-full rounded-lg shadow -mb-16 lg:-mb-32 md:-mb-24" src="../../public/hook.png">
      </div>
    </div>
    <div class="flex flex-row justify-between gap-8">
      <div class="flex basis-1/3 flex-col gap-12 rounded-lg p-10 text-left shadow">
        <img class="w-100 rounded-lg" src="../../public/robots.jpg">
        <div class="description flex flex-col gap-3">
          <p text-3xl font-semibold>
            {{ t('home.benefit-1') }}
          </p>
          <p>{{ t('home.description-1') }}</p>
        </div>
      </div>

      <div class="flex basis-1/3 flex-col gap-12 rounded-lg p-10 text-left shadow">
        <img class="w-100 rounded-lg" src="../../public/machinery.jpg">
        <div class="description flex flex-col gap-3">
          <p text-3xl font-semibold>
            {{ t('home.benefit-2') }}
          </p>
          <p>{{ t('home.description-2') }}</p>
        </div>
      </div>

      <div class="flex basis-1/3 flex-col gap-12 rounded-lg p-10 text-left shadow">
        <img class="w-100 rounded-lg" src="../../public/illustration-4.jpg">
        <div class="description flex flex-col gap-3">
          <p text-3xl font-semibold>
            {{ t('home.benefit-3') }}
          </p>
          <p>{{ t('home.description-3') }}</p>
        </div>
      </div>
    </div>
    <div mx-auto flex flex-col gap-10 rounded-lg p-20 class="sketch-shadow">
      <div flex flex-col gap-3>
        <p text-xl text-orange-400 font-semibold>
          {{ t('home.join-us') }}
        </p>
        <p text-4xl font-bold>
          {{ t('home.future') }}
        </p>
      </div>

      <button offset-2 text-xl underline underline-offset-5>
        {{ t('header.login') }}
      </button>
    </div>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>

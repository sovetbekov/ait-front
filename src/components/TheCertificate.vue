<script>
export default {
  name: 'TheCertificate',
  props: {
    recipientName: {
      type: String,
      required: true,
    },
    courseName: {
      type: String,
      required: true,
    },
    awardDate: {
      type: String,
      required: true,
    },
    issuer: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <div class="certificate border rounded-lg px-8 py-10 text-white shadow" from-cyan-700 to-blue-300 bg-gradient-to-r>
    <div class="flex flex-row items-center justify-center gap-5 text-center">
      <img src="/ait-old-logo.png" width="100">
      <img src="/api.png" width="140">
    </div>
    <div class="header">
      <h1 class="mb-6 text-center text-4xl font-bold">
        Сертификат об успеваемости
      </h1>
    </div>
    <div class="content flex flex-col items-center gap-2 font-italic">
      <p class="text-lg">
        Настоящим подтверждается, что
      </p>
      <h2 class="text-2xl font-bold">
        {{ recipientName }}
      </h2>
      <p class="text-lg">
        успешно завершил курс,
      </p>
      <h3 class="text-xl font-bold">
        {{ courseName }}
      </h3>
      <p class="text-lg">
        присужденный {{ awardDate }}
      </p>
    </div>
    <div class="footer text-right">
      <p class="text-md">
        Выдан: {{ issuer }}
      </p>
    </div>
  </div>
</template>

<style scoped>

</style>

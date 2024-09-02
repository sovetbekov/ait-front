<script setup lang="ts">
import TheCertificate from '~/components/TheCertificate.vue'

const router = useRouter()
</script>

<template>
  <div class="flex flex-row gap-10" min-h-screen>
    <TheSidebar />

    <div class="course-content flex flex-col gap-10 rounded-lg p-10 text-left shadow">
      <div class="course-header">
        <p class="course-name text-3xl font-semibold">
          Инспектор SNT-TC-1A
        </p>

        <div class="stats flex flex-row gap-6">
          <div class="my-4">
            <i class="pi pi-star mr-1 opacity-75" />
            5.0/5.0
          </div>
          <div class="my-4">
            <i class="pi pi-users mr-1 opacity-75" />
            1,921 students
          </div>
          <div class="my-4">
            <i
              class="pi pi-address-book mr-1 opacity-75"
            />
            Владимир Дмитриевич
          </div>
        </div>
        <div class="description my-1 flex items-center rounded-lg opacity-50">
          Академия Индустриальных Технологий предлагает высококачественное образование, соответствующее международным стандартам индустрии. Наша цель - развитие и внедрение инноваций, новых технологий и устойчивого развития в циркулярной промышленности. Мы готовы обеспечить специалистов современными знаниями и практическими навыками.
        </div>
      </div>
      <div class="course-content">
        <p class="mb-2 text-xl font-semibold">
          Содержание курса
        </p>
        <div class="flex flex-row items-center gap-3">
          <p class="opacity-50">
            4 модуля
          </p>
          <p class="opacity-50">
            60 лекций
          </p>
        </div>
      </div>
      <div class="course-sections border rounded-lg">
        <ExpandableSection title="Неделя 1: Введение SNT-TC-1A">
          <TheSubmodule title="Что такое SNT-TC-1A?" @click="router.push('/course/module/ss')" />
          <TheSubmodule title="Возможности новых технологий" />
          <TheSubmodule title="Инновации в промышленной индустрии" />
        </ExpandableSection>
        <ExpandableSection title="Неделя 2: Основы инспектора">
          <p>Content for Module 2</p>
        </ExpandableSection>
        <ExpandableSection title="Неделя 3: Циркулярная промышленность">
          <p>Content for Module 3</p>
        </ExpandableSection>
        <ExpandableSection title="Неделя 4: Инновации в промышленности">
          <p>Content for Module 4</p>
        </ExpandableSection>
        <ExpandableSection title="Неделя 5: Стандарты индустрии">
          <p>Content for Module 5</p>
        </ExpandableSection>
        <ExpandableSection title="Неделя 6: Практические навыки">
          <p>Content for Module 6</p>
        </ExpandableSection>
      </div>
      <div class="">
        <TheCertificate recipient-name="Дастан Сембеков" course-name="Инспектор SNT-TC-1A" award-date="20.08.2024" issuer="AIT.kz (API.org)" />
      </div>
    </div>
  </div>
</template>

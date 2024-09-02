<script>
import { ref } from 'vue'

export default {
  setup() {
    const module = ref({
      title: 'Что такое SNT-TC-1A',
      description: 'Рекомендуемая практика № SNT-TC-1A: Квалификация и сертификация персонала в области неразрушающего контроля (2020) содержит рекомендации для работодателей по созданию внутренних программ сертификации для квалификации и сертификации персонала НК. Она содержит рекомендации по образованию, опыту и обучению для каждого метода НК. С 1966 года работодатели используют этот ценный в отрасли документ в качестве общей основы для своих программ сертификации НК.',
      videoUrl: 'https://www.youtube.com/embed/uE4dLS9357w',
    })

    return {
      module,
    }
  },
}
</script>

<template>
  <div class="flex flex-row gap-10">
    <TheSidebar />
    <div class="module-content flex flex-col gap-10 rounded-lg p-10 text-left shadow">
      <div class="flex flex-row gap-10">
        <div class="mx-auto flex basis-3/4 flex-col text-left container">
          <h1 class="text-2xl font-bold">
            {{ module.title }}
          </h1>
          <p class="mt-2 text-gray-500">
            {{ module.description }}
          </p>

          <div class="mt-10 border rounded-lg p-2">
            <iframe class="h-155 w-full" :src="module.videoUrl" title="API - American Petroleum Institute Spec Q1 Basic Introduction" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen />
          </div>
        </div>
        <div class="other-modules basis-1/4">
          <h1 class="text-xl opacity-80" mb-5>
            Следующие модули
          </h1>
          <div class="module-sections border rounded-lg">
            <ExpandableSection title="Введение SNT-TC-1A">
              <TheSubmodule title="Возможности новых технологий" text-sm />
              <TheSubmodule title="Инновации в промышленной индустрии" text-sm />
            </ExpandableSection>
            <ExpandableSection title="Основы инспектора">
              <p>Content for Module 2</p>
            </ExpandableSection>
            <ExpandableSection title="Циркулярная промышленность">
              <p>Content for Module 3</p>
            </ExpandableSection>
            <ExpandableSection title="Инновации в промышленности">
              <p>Content for Module 4</p>
            </ExpandableSection>
            <ExpandableSection title="Стандарты индустрии">
              <p>Content for Module 5</p>
            </ExpandableSection>
            <ExpandableSection title="Практические навыки">
              <p>Content for Module 6</p>
            </ExpandableSection>
          </div>
        </div>
      </div>
      <div class="quiz-section">
        <h1 class="text-xl font-semibold opacity-80">
          Вопросы для закрепления материала
        </h1>
        <div class="quiz-questions flex flex-col gap-6 py-5">
          <div class="quiz-question">
            <p class="font-bold">
              Вопрос 1:
            </p>
            <p>Что такое Неразрушающий контроль (НК)?</p>
            <div class="quiz-options mt-2 flex flex-row gap-10">
              <label>
                <input type="radio" name="question1" value="option1">
                Вариант 1
              </label>
              <label>
                <input type="radio" name="question1" value="option2">
                Вариант 2
              </label>
              <label>
                <input type="radio" name="question1" value="option3">
                Вариант 3
              </label>
              <label>
                <input type="radio" name="question1" value="option4">
                Вариант 4
              </label>
            </div>
          </div>
          <div class="quiz-question">
            <p class="font-bold">
              Вопрос 2:
            </p>
            <p>Какие методы Неразрушающего контроля (НК) вы знаете?</p>
            <div class="quiz-options mt-2 flex flex-row gap-10">
              <label>
                <input type="radio" name="question2" value="option1">
                Вариант 1
              </label>
              <label>
                <input type="radio" name="question2" value="option2">
                Вариант 2
              </label>
              <label>
                <input type="radio" name="question2" value="option3">
                Вариант 3
              </label>
              <label>
                <input type="radio" name="question2" value="option4">
                Вариант 4
              </label>
            </div>
          </div>
          <div class="quiz-question">
            <p class="font-bold">
              Вопрос 3:
            </p>
            <p>Какие преимущества Неразрушающего контроля (НК) в промышленности?</p>
            <div class="quiz-options mt-2 flex flex-row gap-10">
              <label>
                <input type="radio" name="question3" value="option1">
                Вариант 1
              </label>
              <label>
                <input type="radio" name="question3" value="option2">
                Вариант 2
              </label>
              <label>
                <input type="radio" name="question3" value="option3">
                Вариант 3
              </label>
              <label>
                <input type="radio" name="question3" value="option4">
                Вариант 4
              </label>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
/* Add your Tailwind CSS styles here */
</style>

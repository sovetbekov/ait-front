<script setup lang="ts">
import { ref } from 'vue'

interface Course {
  id: number
  title: string
  description: string
  image: string
}
const { t } = useI18n()

const router = useRouter()

const courses = ref<Course[]>([
  {
    id: 1,
    title: 'Инспектор ACFM (Alternating Current Field Measurement)',
    description: 'Электромагнитный метод для контроля наружных дефектов металла в сварных соединениях',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 2,
    title: 'Инспектор ACPD (Alternating Current Potential Drop)',
    description: 'Метод измерения падения напряжения переменного поля',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 3,
    title: 'Инспектор SNT-TC-1A',
    description: 'Аттестация по методам неразрушающего контроля',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 4,
    title: 'Инспектор LRUT (Long-range Ultrasonic Technology)',
    description: 'Метод направленных волн дальнего действия',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 5,
    title: 'Инспектор SRUT (Short Range Ultrasonics Technology)',
    description: 'Метод ультразвуковых волн ближнего действия',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 6,
    title: 'Инспектор TOFD (Time-of-Flight Diffraction)',
    description: 'Дифракционно-временной метод',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 7,
    title: 'Инспектор PAUT (Phased Array Ultrasonic Testing)',
    description: 'Метод фазированной решеткой',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 8,
    title: 'Инспектор MFL (Magnetic Flux Leakage)',
    description: 'Метод поиска утечек магнитного потока',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 9,
    title: 'Инспектор РЕС (Pulsed Eddy Current)',
    description: 'Импульсный вихретоковый метод',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 10,
    title: 'Инспектор API 570',
    description: 'Нормы и правила инспекции трубопроводов: инспекции, ремонт, модификации и изменение параметров действующих трубопроводных систем',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 11,
    title: 'Инспектор API RP 571',
    description: 'Механизмы повреждения стационарного оборудования в нефтеперерабатывающей промышленности',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 12,
    title: 'Инспектор API 574',
    description: 'Проверка трубопроводов, клапанов и фитингов',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 13,
    title: 'Инспектор API RP 578',
    description: 'Проверка материалов для новых и существующих трубопроводов из сплавов',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 14,
    title: 'Инспектор API 580/581',
    description: 'Контроль основного технологического оборудования с учётом рисков для оборудования под давлением',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 15,
    title: 'Инспектор API 653',
    description: 'Инспекция резервуаров',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 16,
    title: 'Инспектор API 510',
    description: 'Проверка и оценка сосудов под давлением',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 17,
    title: 'Инспектор API 1163',
    description: 'Проверка внутритрубная диагностика',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 18,
    title: 'Инспектор API RP 577',
    description: 'Сварочный контроль и металлургия',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 19,
    title: 'Инспектор API 1104',
    description: 'Сварка при строительстве трубопроводов',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
  {
    id: 20,
    title: 'Инспектор ЕМАТ',
    description: 'Контроль с применением электромагнитных акустических преобразователей',
    image: 'https://img.freepik.com/free-photo/books-with-graduation-cap-digital-art-style-education-day_23-2151164325.jpg',
  },
])
</script>

<template>
  <main
    px-20 py-10
    text="center gray-700 dark:gray-200"
  >
    <div class="courses-container">
      <h1 class="mb-10 text-3xl">
        {{ t('header.courses') }}
      </h1>
      <div class="grid grid-cols-1 gap-10 lg:grid-cols-3 md:grid-cols-2">
        <div v-for="course in courses" :key="course.id" class="course-card">
          <img :src="course.image" alt="Course image" class="course-image">
          <h2 class="course-title">
            {{ course.title }}
          </h2>
          <p class="course-description">
            {{ course.description }}
          </p>
          <button class="button-31" @click="router.push('/course/id')">
            {{ t('button.enroll') }}
          </button>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.courses-container {
  max-width: 1200px;
  margin: 0 auto;
}

.course-card {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 20px;
  text-align: left;
}

.course-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.course-title {
  font-size: 1.5em;
  margin: 10px 0;
}

.course-description {
  margin: 10px 0;
  color: #666;
}

.course-button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.course-button:hover {
  background-color: #0056b3;
}
</style>

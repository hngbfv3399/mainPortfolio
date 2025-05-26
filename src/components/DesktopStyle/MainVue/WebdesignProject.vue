<template>
    <swiper
      :slides-per-view="1"
      :loop="true"
      :autoplay="{ delay: 3000 }"
      class="mySwiper"
    >
      <swiper-slide v-for="project in ProjectLinks" :key="project.link">
        <div>
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" target="_blank" class="btn btn-primary">준비중</a>
        </div>
      </swiper-slide>
    </swiper>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import 'swiper/css'
  import 'swiper/css/navigation'
  import 'swiper/css/pagination'
  
  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
        ProjectLinks: [
          { title: '웹 디자인', description: '준비중', link: '' },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .slide-content {
    padding: 20px;
    border: 2px solid black;
    text-align: center;
  }
  </style>


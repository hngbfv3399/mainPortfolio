<template>
    <swiper
      :slides-per-view="1"
      :loop="true"
      :autoplay="{ delay: 3000 }"
      pagination
      class="mySwiper"
    >
      <swiper-slide v-for="project in ProjectLinks" :key="project.link">
        <div>
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" target="_blank" class="btn btn-primary">보러가기</a>
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
          { title: 'Korea Insider', description: '뉴스 기사 페이지', link: 'https://koreainsider.net/' },
          { title: '당근마켓', description: '당근마켓 클론코딩', link: 'https://hngbfv3399.github.io/vuemarket_clone/' },
          { title: '익명게시판', description: '메모지 형식의 익명게시판', link: 'https://dambaememo.web.app/' },
          { title: '여기어떄', description: '여기어때 클론코딩', link: 'https://hngbfv3399.github.io/badchoicepo/' },


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


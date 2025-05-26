<template>
  <div class="mondrian-app">
    <HeaderVue/>
    <MainVue/>
    <FooterVue/>
  </div>
</template>


<script>

import MainVue from './components/MainVue.vue';
import FooterVue from './components/FooterVue.vue';
import HeaderVue from './components/HeaderVue.vue';
export default{
  components:{
    HeaderVue,
    MainVue,
    FooterVue
  }
}
</script>


<style>
/* 몬드리안 스타일 전역 설정 */
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  background-color: #FEFEFE;
  overflow-x: hidden;
}

.mondrian-app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: #FEFEFE;
}

/* 몬드리안 색상 팔레트 */
:root {
  --mondrian-red: #E60012;
  --mondrian-blue: #0066CC;
  --mondrian-yellow: #FFD700;
  --mondrian-black: #000000;
  --mondrian-white: #FEFEFE;
  --mondrian-gray: #F5F5F5;
}

/* 몬드리안 스타일 보더 */
.mondrian-border {
  border: 4px solid var(--mondrian-black) !important;
}

.mondrian-border-thick {
  border: 8px solid var(--mondrian-black) !important;
}

/* 몬드리안 색상 배경 */
.mondrian-red {
  background-color: var(--mondrian-red);
  color: white;
}

.mondrian-blue {
  background-color: var(--mondrian-blue);
  color: white;
}

.mondrian-yellow {
  background-color: var(--mondrian-yellow);
  color: var(--mondrian-black);
}

.mondrian-white {
  background-color: var(--mondrian-white);
  color: var(--mondrian-black);
}

.mondrian-gray {
  background-color: var(--mondrian-gray);
  color: var(--mondrian-black);
}

/* 타이포그래피 */
h1, h2, h3, h4, h5, h6 {
  font-weight: 700;
  letter-spacing: -0.02em;
  margin: 0;
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .mondrian-border {
    border-width: 3px !important;
  }
  
  .mondrian-border-thick {
    border-width: 5px !important;
  }
  
  .d-flex {
    flex-wrap: wrap !important;
  }
  
  .text-center {
    word-break: break-word;
  }
  
  /* 모바일에서 패딩 조정 */
  .p-3 {
    padding: 1rem !important;
  }
  
  .p-4 {
    padding: 1.5rem !important;
  }
}

@media (max-width: 576px) {
  .mondrian-border {
    border-width: 2px !important;
  }
  
  .mondrian-border-thick {
    border-width: 4px !important;
  }
}

/* 애니메이션 효과 */
.mondrian-hover {
  transition: all 0.3s ease;
}

.mondrian-hover:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

/* 스크롤바 스타일링 */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: var(--mondrian-gray);
}

::-webkit-scrollbar-thumb {
  background: var(--mondrian-black);
  border-radius: 0;
}

::-webkit-scrollbar-thumb:hover {
  background: var(--mondrian-red);
}
</style>

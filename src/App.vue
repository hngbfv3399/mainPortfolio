<template>
  <div style="height: 100vh; display: flex; flex-direction: column; box-sizing: border-box;">
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
.h-40 {
  height: 40%;
}
body {
  margin: 0;
  padding: 0;
}
/* 모바일에서 flex 아이템이 줄바꿈 되도록 */
@media (max-width: 767px) {
  .d-flex {
    flex-wrap: wrap !important; /* flex 줄바꿈 허용 */
  }
  
  /* 텍스트가 너무 길면 줄바꿈 가능하게 */
  .text-center {
    word-break: break-word;
  }
  
  /* 이미지가 넘치지 않도록 */
  
  /* 혹시 내부 박스 간 간격 조금 더 주기 */
  .border {
    padding: 0.5rem; /* 적당히 조절 */
    border: none
  }
}

</style>

<template>
  <div class="row gx-0" style="height: 100vh; box-sizing: border-box;">
    <!-- 왼쪽 사이드 -->
    <div class="col-md-4 col-12 border border-5 border-black d-flex justify-content-center align-items-center">
      <div class="rounded text-center px-3">
        <h1>지호의 포트폴리오</h1>
      </div>
    </div>

    <!-- 오른쪽 컨텐츠 -->
    <div class="col-md-8 col-12 border border-5 border-black d-flex flex-column">
      <div class="container-fluid h-100 p-0 d-flex flex-column">
        <!-- 상단 두 영역: 자기소개 / 연락처 -->
        <div class="row gx-0 flex-grow-1" style="min-height: 0;">
          <IntroVue />
          <div class="col-6 border border-5 border-black d-flex justify-content-center align-items-center">
            연락처
          </div>
        </div>

        <!-- 하단 두 영역: 보유 스킬 / 링크 모음 -->
        <div class="row gx-0 flex-grow-1" style="min-height: 0;">
          <div class="col-6 border border-5 border-black p-3 d-flex flex-column" style="min-height: 0;">
            <h5>보유 스킬</h5>
            <div style="flex: 1 1 auto; min-height: 0;">
              <SkillChart :skills="mySkills" />
            </div>
          </div>
          <div class="col-6 border border-5 border-black d-flex justify-content-center align-items-center">
            링크 모음(깃헙,블로그등)
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import IntroVue from './DesktopStyle/HeaderVue/IntroVue.vue';
import SkillChart from './DesktopStyle/HeaderVue/SkillChart.vue';

export default {
  name: 'HeaderVue',
  components: {
    SkillChart,
    IntroVue,
  },
  data() {
    return {
      mySkills: [
        { name: 'Vue', level: 60 },
        { name: 'React', level: 30 },
        { name: 'Flutter', level: 10 },
        { name: 'Figma', level: 30 },
        { name: 'Firebase', level: 20 },
        { name: 'Express', level: 10 },
        { name: 'Git', level: 70 },
        { name: 'Docker', level: 0 },
      ],
    };
  },
};
</script>

<style scoped>

.col-6 > div > canvas {
  width: 100% !important;
  height: 100% !important;
  display: block;
}
</style>

<template>
  <div class="row gx-0" style="flex: 0 0 40%; box-sizing: border-box;">
      <div class="col-md-10 col-12 border border-5 border-black d-flex justify-content-center align-items-center main-left">
        <div class="container-fluid h-100 p-0">
          <div class="row gx-0" style="height: 50%;">
            <div class="position-relative col-6 border border-5 border-black d-flex justify-content-center align-items-center text-center">
                <div class="position-absolute top-0 start-0 h3">
                    React
                </div>
                <ReactProject/>
            </div>
            <div class="position-relative col-6 border border-5 border-black d-flex justify-content-center align-items-center text-center">
                <div class="position-absolute top-0 start-0 h3">
                    Vue
                </div>
                <VueProject/>
            </div>
          </div>
          <div class="row gx-0" style="height: 50%;">
            <div class="position-relative col-6 border border-5 border-black d-flex justify-content-center align-items-center text-center">
                <div class="position-absolute top-0 start-0 h3">
                    Flutter
                </div>
                <FlutterProject/>
            </div>
            <div class="position-relative col-6 border border-5 border-black d-flex justify-content-center align-items-center text-center">
                <div class="position-absolute top-0 start-0 h3">
                    Web-Design
                </div>
                <WebdesignProject/>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-2 col-12 border border-5 border-black d-flex justify-content-center align-items-center main-right">
        <img src="../assets/profile.jpeg" class="img-thumbnail w-100 h-auto" />
      </div>
    </div>
</template>

<script>
import ReactProject from './DesktopStyle/MainVue/ReactProject.vue';
import VueProject from './DesktopStyle/MainVue/VueProject.vue';
import FlutterProject from './DesktopStyle/MainVue/FlutterProject.vue';
import WebdesignProject from './DesktopStyle/MainVue/WebdesignProject.vue';
export default {
    name: 'MainVue',
    components:{
        ReactProject,
        VueProject,
        FlutterProject,
        WebdesignProject
    }
}
</script>

<style>
@media (max-width: 767px) {
  /* 모바일에서 왼쪽 영역 flex-basis를 70%로 높임 */
  .main-left {
    height: 600px; /* 원하면 높이 조절 가능 */
  }
  /* 모바일에서 이미지 영역 flex-basis를 30%로 줄임 */
  .main-right {
    height: auto;
  }
}
</style>
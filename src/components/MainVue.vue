<template>
  <div class="mondrian-main">
    <!-- 프로젝트 그리드 영역 -->
    <div class="projects-grid">
      <!-- React 프로젝트 - 빨간색 블록 -->
      <div class="project-card mondrian-red mondrian-border mondrian-hover">
        <div class="project-header">
          <h3 class="project-title">React</h3>
          <div class="project-icon"><i class="fab fa-react"></i></div>
        </div>
        <div class="project-content">
          <ReactProject/>
        </div>
      </div>
      
      <!-- Vue 프로젝트 - 파란색 블록 -->
      <div class="project-card mondrian-blue mondrian-border mondrian-hover">
        <div class="project-header">
          <h3 class="project-title">Vue</h3>
          <div class="project-icon"><i class="fab fa-vuejs"></i></div>
        </div>
        <div class="project-content">
          <VueProject/>
        </div>
      </div>
      
      <!-- Flutter 프로젝트 - 노란색 블록 -->
      <div class="project-card mondrian-yellow mondrian-border mondrian-hover">
        <div class="project-header">
          <h3 class="project-title">Flutter</h3>
          <div class="project-icon"><i class="fas fa-mobile-alt"></i></div>
        </div>
        <div class="project-content">
          <FlutterProject/>
        </div>
      </div>
      
      <!-- Web Design 프로젝트 - 흰색 블록 -->
      <div class="project-card mondrian-white mondrian-border mondrian-hover">
        <div class="project-header">
          <h3 class="project-title">Web Design</h3>
          <div class="project-icon"><i class="fas fa-paint-brush"></i></div>
        </div>
        <div class="project-content">
          <WebdesignProject/>
        </div>
      </div>
    </div>

    <!-- 프로필 이미지 영역 - 회색 블록 -->
    <div class="profile-section mondrian-gray mondrian-border">
      <div class="profile-container">
        <div class="profile-image-wrapper">
          <img src="../assets/profile.jpeg" alt="프로필 이미지" class="profile-image" />
          <div class="profile-overlay">
            <div class="profile-info">
              <h4 class="profile-name">김지호</h4>
              <p class="profile-role">Frontend Developer</p>
              <div class="profile-status">
                <span class="status-dot"></span>
                <span class="status-text">Available for work</span>
              </div>
            </div>
          </div>
        </div>
        <div class="profile-stats">
          <div class="stat-item">
            <span class="stat-number"><i class="fas fa-graduation-cap"></i></span>
            <span class="stat-label">신입</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat-item">
            <span class="stat-number">10+</span>
            <span class="stat-label">Projects</span>
          </div>
        </div>
      </div>
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
  components: {
    ReactProject,
    VueProject,
    FlutterProject,
    WebdesignProject
  }
}
</script>

<style scoped>
.mondrian-main {
  display: grid;
  grid-template-columns: 3fr 1fr;
  min-height: 40vh;
  gap: 0;
}

.projects-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 0;
}

.project-card {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
  min-height: 20vh;
  position: relative;
  overflow: hidden;
}

.project-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.project-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin: 0;
}

.project-icon {
  font-size: 2rem;
  color: inherit;
}

.project-icon i {
  color: inherit;
}

.project-content {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.profile-section {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.profile-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
  width: 100%;
}

.profile-image-wrapper {
  position: relative;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  overflow: hidden;
  border: 4px solid var(--mondrian-black);
}

.profile-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.profile-image-wrapper:hover .profile-image {
  transform: scale(1.1);
}

.profile-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0, 0, 0, 0.8));
  color: white;
  padding: 1rem 0.5rem 0.5rem;
  transform: translateY(100%);
  transition: transform 0.3s ease;
}

.profile-image-wrapper:hover .profile-overlay {
  transform: translateY(0);
}

.profile-info {
  text-align: center;
}

.profile-name {
  font-size: 1rem;
  font-weight: 700;
  margin: 0 0 0.25rem 0;
}

.profile-role {
  font-size: 0.8rem;
  margin: 0 0 0.5rem 0;
  opacity: 0.9;
}

.profile-status {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.25rem;
  font-size: 0.7rem;
}

.status-dot {
  width: 6px;
  height: 6px;
  background-color: #4CAF50;
  border-radius: 50%;
}

.profile-stats {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background-color: var(--mondrian-white);
  border: 2px solid var(--mondrian-black);
  width: 100%;
  justify-content: center;
}

.stat-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.25rem;
}

.stat-number {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--mondrian-black);
}

.stat-label {
  font-size: 0.8rem;
  color: var(--mondrian-black);
  opacity: 0.7;
}

.stat-divider {
  width: 1px;
  height: 30px;
  background-color: var(--mondrian-black);
  opacity: 0.3;
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .mondrian-main {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto;
  }
  
  .projects-grid {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
  }
  
  .project-card {
    padding: 1.5rem;
    min-height: 25vh;
  }
  
  .project-title {
    font-size: 1.3rem;
  }
  
  .project-icon {
    font-size: 1.5rem;
  }
  
  .profile-section {
    padding: 2rem;
    min-height: 30vh;
  }
  
  .profile-image-wrapper {
    width: 100px;
    height: 100px;
  }
  
  .profile-stats {
    flex-direction: column;
    gap: 1rem;
    padding: 1.5rem;
  }
  
  .stat-divider {
    width: 30px;
    height: 1px;
  }
}

@media (max-width: 576px) {
  .project-card {
    padding: 1rem;
    min-height: 20vh;
  }
  
  .project-title {
    font-size: 1.2rem;
  }
  
  .project-icon {
    font-size: 1.3rem;
  }
  
  .profile-section {
    padding: 1.5rem;
  }
  
  .profile-image-wrapper {
    width: 80px;
    height: 80px;
  }
  
  .profile-name {
    font-size: 0.9rem;
  }
  
  .profile-role {
    font-size: 0.7rem;
  }
  
  .stat-number {
    font-size: 1.2rem;
  }
  
  .stat-label {
    font-size: 0.7rem;
  }
}

/* 프로젝트 컴포넌트 스타일 오버라이드 */
.project-content :deep(*) {
  color: inherit;
}
</style>
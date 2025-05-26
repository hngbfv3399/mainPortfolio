<template>
  <div class="mondrian-header">
    <!-- 왼쪽 타이틀 영역 - 빨간색 블록 -->
    <div class="title-section mondrian-red mondrian-border-thick">
      <div class="title-content">
        <h1 class="portfolio-title">지호의<br>포트폴리오</h1>
        <div class="title-accent"></div>
      </div>
    </div>

    <!-- 오른쪽 정보 그리드 -->
    <div class="info-grid">
      <!-- 자기소개 영역 - 노란색 블록 -->
      <div class="intro-section mondrian-yellow mondrian-border">
        <IntroVue />
      </div>
      
      <!-- 연락처 영역 - 파란색 블록 -->
      <div class="contact-section mondrian-blue mondrian-border">
        <div class="contact-content">
          <h3><i class="fas fa-address-book"></i> 연락처</h3>
          <div class="contact-info">
            <div class="contact-item">
              <i class="fas fa-envelope contact-icon"></i>
              <span>hngbfv3399@gmail.com</span>
            </div>
            <div class="contact-item">
              <i class="fas fa-mobile-alt contact-icon"></i>
              <span>010-3942-2836</span>
            </div>
          </div>
        </div>
      </div>

      <!-- 스킬 영역 - 흰색 블록 -->
      <div class="skills-section mondrian-white mondrian-border">
        <h3><i class="fas fa-code"></i> 보유 스킬</h3>
        <div class="skills-chart-container">
          <SkillChart :skills="mySkills" />
        </div>
      </div>
      
      <!-- 링크 영역 - 회색 블록 -->
      <div class="links-section mondrian-gray mondrian-border mondrian-hover">
        <div class="links-content">
          <h3><i class="fas fa-link"></i> 링크 모음</h3>
          <div class="social-links">
            <a href="https://github.com/hngbfv3399" class="social-link github">
              <i class="fab fa-github link-icon"></i>
              <span>GitHub</span>
            </a>
            <a href="#" class="social-link blog">
              <i class="fas fa-blog link-icon"></i>
              <span>Blog</span>
            </a>
            <a href="#" class="social-link linkedin">
              <i class="fab fa-linkedin link-icon"></i>
              <span>LinkedIn</span>
            </a>
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
.mondrian-header {
  display: grid;
  grid-template-columns: 1fr 2fr;
  min-height: 60vh;
  gap: 0;
}

.title-section {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 3rem;
  position: relative;
  overflow: hidden;
}

.title-content {
  text-align: center;
  position: relative;
  z-index: 2;
}

.portfolio-title {
  font-size: 3.5rem;
  font-weight: 900;
  line-height: 0.9;
  text-transform: uppercase;
  letter-spacing: -0.05em;
  margin-bottom: 1rem;
}

.title-accent {
  width: 60px;
  height: 8px;
  background-color: white;
  margin: 0 auto;
}

.info-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 0;
}

.intro-section,
.contact-section,
.skills-section,
.links-section {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  min-height: 30vh;
}

.contact-content h3,
.skills-section h3,
.links-content h3 {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  font-weight: 700;
}

.contact-content h3 i,
.skills-section h3 i,
.links-content h3 i {
  margin-right: 0.5rem;
  color: inherit;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1.1rem;
}

.contact-icon {
  font-size: 1.2rem;
  width: 20px;
  text-align: center;
}

.skills-chart-container {
  width: 100%;
  height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.social-links {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
}

.social-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1rem;
  background-color: var(--mondrian-white);
  color: var(--mondrian-black);
  text-decoration: none;
  border: 2px solid var(--mondrian-black);
  transition: all 0.3s ease;
  font-weight: 600;
}

.social-link:hover {
  background-color: var(--mondrian-black);
  color: var(--mondrian-white);
  transform: translateX(5px);
}

.link-icon {
  font-size: 1.2rem;
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .mondrian-header {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto;
    min-height: auto;
  }
  
  .title-section {
    padding: 2rem;
    min-height: 40vh;
  }
  
  .portfolio-title {
    font-size: 2.5rem;
  }
  
  .info-grid {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
  }
  
  .intro-section,
  .contact-section,
  .skills-section,
  .links-section {
    padding: 1.5rem;
    min-height: 25vh;
  }
  
  .skills-chart-container {
    height: 150px;
  }
  
  .social-links {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .social-link {
    flex: 1;
    min-width: 120px;
    justify-content: center;
  }
}

@media (max-width: 576px) {
  .title-section {
    padding: 1.5rem;
  }
  
  .portfolio-title {
    font-size: 2rem;
  }
  
  .intro-section,
  .contact-section,
  .skills-section,
  .links-section {
    padding: 1rem;
    min-height: 20vh;
  }
  
  .contact-info {
    gap: 0.75rem;
  }
  
  .contact-item {
    font-size: 1rem;
  }
  
  .social-links {
    flex-direction: column;
  }
  
  .social-link {
    min-width: auto;
  }
}

/* 차트 스타일 오버라이드 */
.skills-section :deep(canvas) {
  max-width: 100% !important;
  max-height: 100% !important;
}
</style>

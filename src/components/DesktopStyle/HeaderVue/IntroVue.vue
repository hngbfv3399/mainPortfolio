<template>
  <div class="intro-container">
    <h3 class="intro-title"><i class="fas fa-user-circle"></i> 자기소개</h3>
    <div class="intro-content">
      <p class="intro-text">
        안녕하세요! 창의적이고 열정적인 
        <strong>프론트엔드 개발자</strong> 김지호입니다.
      </p>
      <p class="intro-text">
        사용자 경험을 중시하며, 
        <strong>Vue.js</strong>와 <strong>React</strong>를 
        활용한 모던 웹 개발에 집중하고 있습니다.
      </p>
      <div class="intro-highlight">
        <span class="highlight-text"><i class="fas fa-code"></i> Clean Code</span>
        <span class="highlight-divider">•</span>
        <span class="highlight-text"><i class="fas fa-palette"></i> UX/UI</span>
        <span class="highlight-divider">•</span>
        <span class="highlight-text"><i class="fas fa-lightbulb"></i> Innovation</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.intro-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 1rem;
}

.intro-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  color: var(--mondrian-black);
}

.intro-title i {
  margin-right: 0.5rem;
  color: var(--mondrian-black);
}

.intro-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 280px;
}

.intro-text {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--mondrian-black);
  margin: 0;
  font-weight: 400;
}

.intro-text strong {
  font-weight: 700;
  color: var(--mondrian-black);
}

.intro-highlight {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  margin-top: 1rem;
  padding: 0.75rem;
  background-color: rgba(0, 0, 0, 0.1);
  border-radius: 0;
}

.highlight-text {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--mondrian-black);
  display: flex;
  align-items: center;
  gap: 0.25rem;
}

.highlight-text i {
  font-size: 0.8rem;
}

.highlight-divider {
  font-weight: 700;
  color: var(--mondrian-black);
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .intro-content {
    max-width: 250px;
  }
  
  .intro-text {
    font-size: 0.95rem;
  }
  
  .intro-highlight {
    flex-direction: column;
    gap: 0.25rem;
  }
  
  .highlight-divider {
    display: none;
  }
}

@media (max-width: 576px) {
  .intro-container {
    padding: 0.5rem;
  }
  
  .intro-title {
    font-size: 1.3rem;
    margin-bottom: 1rem;
  }
  
  .intro-content {
    max-width: 220px;
    gap: 0.75rem;
  }
  
  .intro-text {
    font-size: 0.9rem;
  }
  
  .highlight-text {
    font-size: 0.8rem;
  }
}
</style>
  
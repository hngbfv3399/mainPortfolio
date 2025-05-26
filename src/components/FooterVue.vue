<template>
  <div class="mondrian-footer">
    <!-- 메인 메시지 영역 - 빨간색 블록 -->
    <div class="footer-message mondrian-red mondrian-border">
      <div class="message-content">
        <h3 class="footer-title"><i class="fas fa-heart"></i> 감사합니다!</h3>
        <p class="footer-subtitle">기술과 감성을 잇는 개발자 김지호입니다.</p>
        <div class="message-accent"></div>
      </div>
    </div>

    <!-- 연락처 정보 영역 - 파란색 블록 -->
    <div class="footer-contact mondrian-blue mondrian-border">
      <div class="contact-content">
        <h4 class="contact-title"><i class="fas fa-handshake"></i> Let's Connect</h4>
        <p class="contact-description">궁금한 점이 있다면 언제든지 연락 주세요.</p>
        
        <button class="contact-button mondrian-hover">
          <i class="fas fa-envelope button-icon"></i>
          <span>Contact Me</span>
        </button>
      </div>
    </div>

    <!-- 링크 정보 영역 - 노란색 블록 -->
    <div class="footer-links mondrian-yellow mondrian-border">
      <div class="links-content">
        <div class="link-item">
          <i class="fas fa-envelope link-icon"></i>
          <span class="link-text">hngbfv3399@gmail.com</span>
        </div>
        <div class="link-item">
          <i class="fab fa-github link-icon"></i>
          <a href="https://github.com/hngbfv3399" target="_blank" class="link-text">
            github.com/hngbfv3399
          </a>
        </div>
      </div>
    </div>

    <!-- 저작권 정보 영역 - 흰색 블록 -->
    <div class="footer-copyright mondrian-white mondrian-border">
      <div class="copyright-content">
        <div class="year-badge">2025</div>
        <p class="copyright-text">
          &copy; 김지호 Portfolio.<br>
          All rights reserved.
        </p>
        <div class="made-with">
          <span>Made with</span>
          <i class="fas fa-heart heart"></i>
          <span>& Vue.js</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FooterVue',
};
</script>

<style scoped>
.mondrian-footer {
  display: grid;
  grid-template-columns: 2fr 2fr 2fr 1fr;
  min-height: 25vh;
  gap: 0;
}

.footer-message,
.footer-contact,
.footer-links,
.footer-copyright {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.message-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.footer-title {
  font-size: 2rem;
  font-weight: 900;
  margin: 0;
  text-transform: uppercase;
  letter-spacing: -0.02em;
}

.footer-title i {
  margin-right: 0.5rem;
  color: inherit;
}

.footer-subtitle {
  font-size: 1.1rem;
  margin: 0;
  line-height: 1.5;
  font-weight: 400;
}

.message-accent {
  width: 50px;
  height: 4px;
  background-color: white;
}

.contact-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}

.contact-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin: 0;
}

.contact-title i {
  margin-right: 0.5rem;
  color: inherit;
}

.contact-description {
  font-size: 1rem;
  margin: 0;
  line-height: 1.5;
}

.contact-button {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  background-color: var(--mondrian-white);
  color: var(--mondrian-black);
  border: 3px solid var(--mondrian-black);
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.contact-button:hover {
  background-color: var(--mondrian-black);
  color: var(--mondrian-white);
  transform: translateY(-2px);
}

.button-icon {
  font-size: 1.2rem;
}

.links-content {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  width: 100%;
}

.link-item {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem;
  background-color: rgba(0, 0, 0, 0.1);
  border-radius: 0;
}

.link-icon {
  font-size: 1.2rem;
  flex-shrink: 0;
  width: 20px;
  text-align: center;
}

.link-text {
  font-size: 0.9rem;
  font-weight: 500;
  color: var(--mondrian-black);
  text-decoration: none;
  word-break: break-all;
}

.link-text:hover {
  text-decoration: underline;
}

.copyright-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.year-badge {
  font-size: 2rem;
  font-weight: 900;
  color: var(--mondrian-black);
  border: 3px solid var(--mondrian-black);
  padding: 0.5rem 1rem;
  background-color: var(--mondrian-gray);
}

.copyright-text {
  font-size: 0.8rem;
  margin: 0;
  line-height: 1.4;
  color: var(--mondrian-black);
  opacity: 0.8;
}

.made-with {
  display: flex;
  align-items: center;
  gap: 0.25rem;
  font-size: 0.7rem;
  color: var(--mondrian-black);
  opacity: 0.7;
}

.heart {
  color: var(--mondrian-red);
  animation: heartbeat 2s ease-in-out infinite;
}

@keyframes heartbeat {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.1); }
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .mondrian-footer {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
  }
  
  .footer-message,
  .footer-contact,
  .footer-links,
  .footer-copyright {
    padding: 1.5rem;
    min-height: 20vh;
  }
  
  .footer-title {
    font-size: 1.5rem;
  }
  
  .footer-subtitle {
    font-size: 1rem;
  }
  
  .contact-title {
    font-size: 1.3rem;
  }
  
  .contact-description {
    font-size: 0.9rem;
  }
  
  .contact-button {
    padding: 0.75rem 1.5rem;
    font-size: 0.9rem;
  }
  
  .link-item {
    flex-direction: column;
    text-align: center;
    gap: 0.5rem;
  }
  
  .year-badge {
    font-size: 1.5rem;
    padding: 0.4rem 0.8rem;
  }
}

@media (max-width: 576px) {
  .footer-message,
  .footer-contact,
  .footer-links,
  .footer-copyright {
    padding: 1rem;
    min-height: 15vh;
  }
  
  .footer-title {
    font-size: 1.3rem;
  }
  
  .footer-subtitle {
    font-size: 0.9rem;
  }
  
  .contact-title {
    font-size: 1.2rem;
  }
  
  .contact-description {
    font-size: 0.8rem;
  }
  
  .contact-button {
    padding: 0.6rem 1.2rem;
    font-size: 0.8rem;
  }
  
  .link-text {
    font-size: 0.8rem;
  }
  
  .year-badge {
    font-size: 1.2rem;
    padding: 0.3rem 0.6rem;
  }
  
  .copyright-text {
    font-size: 0.7rem;
  }
  
  .made-with {
    font-size: 0.6rem;
  }
}
</style>

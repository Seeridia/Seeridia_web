<template>
  <div class="grid-container">
    <!-- Geometric Background Elements -->
    <div class="geometric-element circle-1"></div>
    <div class="geometric-element rectangle-1"></div>
    <div class="geometric-element line-1"></div>
    <div class="geometric-element line-2"></div>
    
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-grid">
        <div class="name-block">
          <h1 class="name">Seeridia</h1>
          <div class="red-accent-bar"></div>
        </div>
        <div class="title-block">
          <p class="title">developer</p>
          <p class="title">& designer</p>
        </div>
        <div class="diagonal-element"></div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about">
      <div class="section-grid">
        <div class="section-header">
          <h2>about</h2>
          <div class="section-number">01</div>
        </div>
        <div class="content-block">
          <div class="motto-container">
            <p class="motto">让繁复归于简洁</p>
            <p class="motto">让生硬化作温柔</p>
          </div>
          <div class="description">
            <p>我是一名充满热情的全栈开发者，目前就读于福州大学。致力于通过代码与设计的完美结合，创造出既美观又实用的数字产品。</p>
            <p>我相信技术应该服务于人，让复杂的事情变得简单而优雅。</p>
          </div>
        </div>
        <div class="geometric-accent"></div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="skills">
      <div class="section-grid">
        <div class="section-header">
          <h2>expertise</h2>
          <div class="section-number">02</div>
        </div>
        <div class="skills-layout">
          <div class="skill-item">
            <div class="skill-label">web development</div>
            <div class="skill-description">精通 vue.js、react 等现代前端框架，构建高性能的 web 应用</div>
          </div>
          <div class="skill-item">
            <div class="skill-label">mobile development</div>
            <div class="skill-description">使用 flutter 构建原生级移动应用，专注用户体验与性能优化</div>
          </div>
          <div class="skill-item">
            <div class="skill-label">design thinking</div>
            <div class="skill-description">深度理解用户体验设计原则，从概念到实现的全流程把控</div>
          </div>
        </div>
        <div class="skills-geometric"></div>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="projects">
      <div class="section-grid">
        <div class="section-header">
          <h2>featured work</h2>
          <div class="section-number">03</div>
        </div>
        <div class="projects-layout">
          <div class="project-item">
            <div class="project-meta">
              <div class="project-number">01</div>
              <div class="project-title">Alto typora theme</div>
            </div>
            <div class="project-description">
              <p>为 typora 编辑器精心设计的优雅主题，专注于提升写作与思考的沉浸体验。通过细致的排版与配色，让每一次创作都成为视觉享受。</p>
              <a href="https://github.com/Seeridia/typora-theme-alto" target="_blank" class="project-link">
                探索项目 →
              </a>
            </div>
          </div>
          
          <div class="project-item">
            <div class="project-meta">
              <div class="project-number">02</div>
              <div class="project-title">shotmeld</div>
            </div>
            <div class="project-description">
              <p>高颜值的在线照片存储与管理平台。结合现代设计语言与直观的交互体验，让照片管理变得简单而愉悦。</p>
              <a href="https://github.com/ShotMeld/Shotmeld-web" target="_blank" class="project-link">
                探索项目 →
              </a>
            </div>
          </div>
          
          <div class="project-item">
            <div class="project-meta">
              <div class="project-number">03</div>
              <div class="project-title">flct 预约助手</div>
            </div>
            <div class="project-description">
              <p>专为福州大学学习中心打造的移动端预约应用。使用 flutter 构建，提供流畅的跨平台体验与便捷的预约流程。</p>
              <a href="https://github.com/Seeridia/FLCT" target="_blank" class="project-link">
                探索项目 →
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact">
      <div class="section-grid">
        <div class="section-header">
          <h2>connect</h2>
          <div class="section-number">04</div>
        </div>
        <div class="contact-layout">
          <div class="contact-links">
            <a href="https://github.com/Seeridia" target="_blank" class="contact-link">
              <span class="link-label">github</span>
              <span class="link-arrow">→</span>
            </a>
            <a href="https://zhihu.com/people/seeridia" target="_blank" class="contact-link">
              <span class="link-label">知乎</span>
              <span class="link-arrow">→</span>
            </a>
            <a href="mailto:seeridia@gmail.com" class="contact-link">
              <span class="link-label">email</span>
              <span class="link-arrow">→</span>
            </a>
          </div>
        </div>
        <div class="contact-geometric"></div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="footer-grid">
        <div class="footer-info">
          <p>&copy; 2025 Seeridia</p>
        </div>
        <div class="beian-info">
          <a href="https://beian.miit.gov.cn" target="_blank" rel="noopener noreferrer">
            闽icp备2025099091号
          </a>
          <a href="https://beian.mps.gov.cn/#/query/webSearch?code=35018302000247" rel="noreferrer" target="_blank">
            闽公网安备35018302000247号
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'

onMounted(() => {
  // 检测用户系统偏好的主题
  const prefersDark = window.matchMedia('(prefers-color-scheme: dark)')
  
  // 应用初始主题
  applyTheme(prefersDark.matches)
  
  // 监听系统主题变化
  prefersDark.addEventListener('change', (e) => {
    applyTheme(e.matches)
  })
})

function applyTheme(isDark: boolean) {
  if (isDark) {
    document.documentElement.classList.add('dark')
  } else {
    document.documentElement.classList.remove('dark')
  }
}
</script>

<style>
/* CSS Reset & Base Typography */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  --bg-primary: #FFFFFF;
  --bg-secondary: #F5F5F5;
  --text-primary: #111111;
  --text-secondary: #333333;
  --text-tertiary: #666666;
  --accent-red: #E60000;
  --border-color: rgba(17, 17, 17, 0.1);
  --grid-gap: 24px;
  --section-padding: 120px;
  
  font-family: 'Inter', 'Helvetica Neue', 'Arial', sans-serif;
  font-feature-settings: "liga" 1, "kern" 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  line-height: 1.2;
}

html.dark {
  --bg-primary: #000000;
  --bg-secondary: #111111;
  --text-primary: #FFFFFF;
  --text-secondary: #CCCCCC;
  --text-tertiary: #999999;
  --accent-red: #FF0000;
  --border-color: rgba(255, 255, 255, 0.1);
}

body {
  background-color: var(--bg-primary);
  color: var(--text-primary);
  font-size: 16px;
  overflow-x: hidden;
}

/* Grid System - 12 Column Layout */
.grid-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--grid-gap);
  position: relative;
  background-color: var(--bg-primary);
  transition: background-color 0.3s ease;
}

.section-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: var(--grid-gap);
  align-items: start;
  position: relative;
}

/* Geometric Background Elements */
.geometric-element {
  position: fixed;
  z-index: -1;
  transition: all 0.3s ease;
}

.circle-1 {
  width: 200px;
  height: 200px;
  background-color: var(--accent-red);
  border-radius: 50%;
  top: 15%;
  right: -100px;
  opacity: 0.8;
}

.rectangle-1 {
  width: 4px;
  height: 100vh;
  background-color: var(--text-primary);
  top: 0;
  left: 20%;
  opacity: 0.1;
}

.line-1 {
  width: 100%;
  height: 2px;
  background-color: var(--accent-red);
  top: 40%;
  left: 0;
  transform: rotate(-15deg);
  opacity: 0.3;
}

.line-2 {
  width: 60%;
  height: 1px;
  background-color: var(--text-primary);
  bottom: 30%;
  right: 0;
  transform: rotate(25deg);
  opacity: 0.2;
}

/* Hero Section */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.hero-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: var(--grid-gap);
  width: 100%;
  align-items: center;
}

.name-block {
  grid-column: 1 / 8;
  position: relative;
}

.name {
  font-size: clamp(4rem, 12vw, 8rem);
  font-weight: 900;
  text-transform: lowercase;
  letter-spacing: -0.04em;
  line-height: 0.85;
  color: var(--text-primary);
  margin: 0;
  position: relative;
}

.red-accent-bar {
  width: 120px;
  height: 8px;
  background-color: var(--accent-red);
  margin-top: 16px;
  transform: translateX(-4px);
}

.title-block {
  grid-column: 9 / 13;
  text-align: right;
}

.title {
  font-size: 1.5rem;
  font-weight: 300;
  text-transform: lowercase;
  color: var(--text-secondary);
  margin: 0;
  line-height: 1.2;
}

.diagonal-element {
  position: absolute;
  width: 300px;
  height: 2px;
  background-color: var(--accent-red);
  top: 60%;
  right: 10%;
  transform: rotate(-30deg);
  opacity: 0.6;
}

/* Section Headers */
.section-header {
  grid-column: 1 / 4;
  position: relative;
  margin-bottom: 48px;
}

.section-header h2 {
  font-size: 3rem;
  font-weight: 700;
  text-transform: lowercase;
  letter-spacing: -0.02em;
  color: var(--text-primary);
  margin: 0;
  line-height: 0.9;
}

.section-number {
  font-size: 1rem;
  font-weight: 400;
  color: var(--accent-red);
  margin-top: 8px;
  font-family: 'Courier New', monospace;
}

/* Sections */
section {
  padding: var(--section-padding) 0;
  position: relative;
}

section:not(.hero) {
  border-top: 1px solid var(--border-color);
}

/* About Section */
.content-block {
  grid-column: 5 / 11;
}

.motto-container {
  margin-bottom: 48px;
}

.motto {
  font-size: 1.5rem;
  font-weight: 500;
  color: var(--text-primary);
  margin: 0 0 8px 0;
  line-height: 1.3;
  text-transform: none;
}

.description {
  font-size: 1.125rem;
  line-height: 1.6;
  color: var(--text-secondary);
}

.description p {
  margin: 0 0 24px 0;
}

.description p:last-child {
  margin-bottom: 0;
}

.geometric-accent {
  grid-column: 11 / 13;
  height: 200px;
  background-color: var(--accent-red);
  width: 4px;
  justify-self: center;
  opacity: 0.8;
}

/* Skills Section */
.skills-layout {
  grid-column: 4 / 12;
  display: grid;
  grid-template-columns: 1fr;
  gap: 48px;
}

.skill-item {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: var(--grid-gap);
  align-items: baseline;
  padding: 24px 0;
  border-bottom: 1px solid var(--border-color);
}

.skill-item:last-child {
  border-bottom: none;
}

.skill-label {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-primary);
  text-transform: lowercase;
}

.skill-description {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--text-secondary);
}

.skills-geometric {
  grid-column: 1 / 3;
  width: 100px;
  height: 100px;
  border: 2px solid var(--accent-red);
  transform: rotate(45deg);
  align-self: center;
  justify-self: center;
}

/* Projects Section */
.projects-layout {
  grid-column: 1 / 13;
  display: grid;
  grid-template-columns: 1fr;
  gap: 64px;
  margin-top: 48px;
}

.project-item {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 48px;
  align-items: start;
  padding: 48px 0;
  border-bottom: 1px solid var(--border-color);
  position: relative;
}

.project-item:last-child {
  border-bottom: none;
}

.project-meta {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.project-number {
  font-size: 3rem;
  font-weight: 900;
  color: var(--accent-red);
  line-height: 1;
  font-family: 'Courier New', monospace;
}

.project-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--text-primary);
  text-transform: lowercase;
  line-height: 1.2;
}

.project-description {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.project-description p {
  font-size: 1.125rem;
  line-height: 1.6;
  color: var(--text-secondary);
  margin: 0;
}

.project-link {
  font-size: 1rem;
  font-weight: 500;
  color: var(--accent-red);
  text-decoration: none;
  text-transform: lowercase;
  transition: all 0.2s ease;
  align-self: flex-start;
}

.project-link:hover {
  color: var(--text-primary);
  background-color: var(--accent-red);
  padding: 4px 8px;
  margin: -4px -8px;
}

/* Contact Section */
.contact-layout {
  grid-column: 4 / 10;
}

.contact-links {
  display: flex;
  flex-direction: column;
  gap: 32px;
}

.contact-link {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 24px 0;
  border-bottom: 1px solid var(--border-color);
  text-decoration: none;
  transition: all 0.2s ease;
  color: var(--text-primary);
}

.contact-link:hover {
  border-color: var(--accent-red);
  transform: translateX(8px);
}

.contact-link:hover .link-arrow {
  color: var(--accent-red);
}

.link-label {
  font-size: 1.5rem;
  font-weight: 500;
  text-transform: lowercase;
}

.link-arrow {
  font-size: 1.5rem;
  font-weight: 300;
  transition: color 0.2s ease;
}

.contact-geometric {
  grid-column: 10 / 12;
  width: 80px;
  height: 80px;
  background-color: var(--accent-red);
  border-radius: 50%;
  align-self: center;
  justify-self: center;
  opacity: 0.8;
}

/* Footer */
.footer {
  padding: 48px 0;
  border-top: 1px solid var(--border-color);
}

.footer-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: var(--grid-gap);
  align-items: center;
}

.footer-info {
  grid-column: 1 / 4;
}

.footer-info p {
  font-size: 0.875rem;
  color: var(--text-tertiary);
  margin: 0;
  text-transform: lowercase;
}

.beian-info {
  grid-column: 9 / 13;
  display: flex;
  gap: 24px;
  justify-content: flex-end;
  flex-wrap: wrap;
}

.beian-info a {
  font-size: 0.75rem;
  color: var(--text-tertiary);
  text-decoration: none;
  text-transform: lowercase;
  transition: color 0.2s ease;
}

.beian-info a:hover {
  color: var(--text-secondary);
}

/* Responsive Design */
@media (max-width: 1024px) {
  .grid-container {
    max-width: 100%;
    padding: 0 var(--grid-gap);
  }
  
  .hero-grid {
    grid-template-columns: 1fr;
    gap: 48px;
    text-align: left;
  }
  
  .name-block,
  .title-block {
    grid-column: 1 / -1;
  }
  
  .title-block {
    text-align: left;
  }
  
  .section-header {
    grid-column: 1 / -1;
    margin-bottom: 32px;
  }
  
  .content-block,
  .skills-layout,
  .contact-layout {
    grid-column: 1 / -1;
  }
  
  .skill-item,
  .project-item {
    grid-template-columns: 1fr;
    gap: 24px;
  }
  
  .geometric-accent,
  .skills-geometric,
  .contact-geometric {
    display: none;
  }
}

@media (max-width: 768px) {
  html {
    --section-padding: 80px;
    --grid-gap: 16px;
  }
  
  .name {
    font-size: clamp(3rem, 10vw, 6rem);
  }
  
  .section-header h2 {
    font-size: 2.5rem;
  }
  
  .projects-layout {
    gap: 48px;
  }
  
  .project-item {
    padding: 32px 0;
  }
  
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }
  
  .footer-info {
    grid-column: 1 / -1;
  }
  
  .beian-info {
    grid-column: 1 / -1;
    justify-content: flex-start;
    flex-direction: column;
    gap: 8px;
  }
}

@media (max-width: 480px) {
  .circle-1 {
    width: 120px;
    height: 120px;
    right: -60px;
  }
  
  .contact-links {
    gap: 24px;
  }
  
  .contact-link {
    padding: 16px 0;
  }
}

/* Dark mode specific adjustments */
html.dark .geometric-element {
  mix-blend-mode: screen;
}

html.dark .project-link:hover {
  color: var(--bg-primary);
}
</style>

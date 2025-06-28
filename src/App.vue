<template>
  <div class="container">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-content">
        <h1 class="name">Seeridia</h1>
        <p class="title">Developer & Designer</p>
      </div>
    </section>

    <!-- About Section -->
    <section class="about">
      <div class="section-content">
        <h2>About Me</h2>
        <p class="motto">让繁复归于简洁，让生硬化作温柔</p>
        <p>我是一名充满热情的全栈开发者，目前就读于福州大学。致力于通过代码与设计的完美结合，创造出既美观又实用的数字产品。我相信技术应该服务于人，让复杂的事情变得简单而优雅。</p>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="skills">
      <div class="section-content">
        <h2>Expertise</h2>
        <div class="skills-grid">
          <div class="skill-card">
            <h3>Web 开发</h3>
            <p>精通 Vue.js、React 等现代前端框架，构建高性能的 Web 应用</p>
          </div>
          <div class="skill-card">
            <h3>移动开发</h3>
            <p>使用 Flutter 构建原生级移动应用，专注用户体验与性能优化</p>
          </div>
          <div class="skill-card">
            <h3>设计思维</h3>
            <p>深度理解用户体验设计原则，从概念到实现的全流程把控</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="projects">
      <div class="section-content">
        <h2>Featured Work</h2>
        <div class="projects-grid">
          <div class="project-card">
            <h3>Alto Typora Theme</h3>
            <p>为 Typora 编辑器精心设计的优雅主题，专注于提升写作与思考的沉浸体验。通过细致的排版与配色，让每一次创作都成为视觉享受。</p>
            <a href="https://github.com/Seeridia/typora-theme-alto" target="_blank" class="project-link">探索项目</a>
          </div>
          <div class="project-card">
            <h3>ShotMeld</h3>
            <p>高颜值的在线照片存储与管理平台。结合现代设计语言与直观的交互体验，让照片管理变得简单而愉悦。</p>
            <a href="https://github.com/ShotMeld/Shotmeld-web" target="_blank" class="project-link">探索项目</a>
          </div>
          <div class="project-card">
            <h3>FLCT 预约助手</h3>
            <p>专为福州大学学习中心打造的移动端预约应用。使用 Flutter 构建，提供流畅的跨平台体验与便捷的预约流程。</p>
            <a href="https://github.com/Seeridia/FLCT" target="_blank" class="project-link">探索项目</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact">
      <div class="section-content">
        <h2>Let's Connect</h2>
        <div class="contact-links">
          <a href="https://github.com/Seeridia" target="_blank" class="contact-link">GitHub</a>
          <a href="https://zhihu.com/people/seeridia" target="_blank" class="contact-link">知乎</a>
          <a href="mailto:seeridia@gmail.com" class="contact-link">Email</a>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <p>&copy; 2025 Seeridia. All rights reserved.</p>
      <div class="beian-info">
        <a href="https://beian.miit.gov.cn" target="_blank" rel="noopener noreferrer">
          闽ICP备2025099091号
        </a>
        <a
          href="https://beian.mps.gov.cn/#/query/webSearch?code=35018302000247"
          rel="noreferrer"
          target="_blank"
        >
          闽公网安备35018302000247号
        </a>
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
html {
  --bg-primary: #ffffff;
  --bg-secondary: #fbfbfd;
  --bg-card: #fbfbfd;
  --text-primary: #1d1d1f;
  --text-secondary: #515154;
  --text-tertiary: #86868b;
  --border-color: #f5f5f7;
  --accent-color: #0071e3;
  --gradient-start: #1d1d1f;
  --gradient-end: #86868b;
  
  background-color: var(--bg-primary);
  color: var(--text-primary);
  transition: background-color 0.3s ease, color 0.3s ease;
}

html.dark {
  --bg-primary: #000000;
  --bg-secondary: #1c1c1e;
  --bg-card: #1c1c1e;
  --text-primary: #ffffff;
  --text-secondary: #d1d1d6;
  --text-tertiary: #8e8e93;
  --border-color: #38383a;
  --accent-color: #007aff;
  --gradient-start: #ffffff;
  --gradient-end: #8e8e93;
}

body {
  background-color: var(--bg-primary);
  color: var(--text-primary);
  margin: 0;
  padding: 0;
}

.container {
  max-width: 980px;
  margin: 0 auto;
  padding: 0 20px;
  background-color: var(--bg-primary);
}

.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.hero-content .name {
  font-size: 4rem;
  font-weight: 600;
  margin: 0;
  letter-spacing: -0.02em;
  color: var(--text-primary);
}

html:not(.dark) .hero-content .name {
  background: linear-gradient(135deg, #1d1d1f 0%, #86868b 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

html.dark .hero-content .name {
  color: var(--text-primary);
}

.hero-content .title {
  font-size: 1.5rem;
  font-weight: 400;
  color: var(--text-tertiary);
  margin: 1rem 0 0.5rem 0;
}

section {
  padding: 80px 0;
  border-bottom: 1px solid var(--border-color);
}

section:last-of-type {
  border-bottom: none;
}

.section-content {
  max-width: 800px;
  margin: 0 auto;
}

h2 {
  font-size: 2.5rem;
  font-weight: 600;
  text-align: center;
  margin-bottom: 3rem;
  color: var(--text-primary);
  letter-spacing: -0.01em;
}

.about p {
  font-size: 1.25rem;
  line-height: 1.6;
  color: var(--text-secondary);
  text-align: center;
  max-width: 600px;
  margin: 0 auto;
}

.about .motto {
  font-size: 1.5rem;
  font-weight: 500;
  color: var(--text-primary);
  font-style: italic;
  margin-bottom: 2rem;
  position: relative;
}

.about .motto::before,
.about .motto::after {
  content: '"';
  color: var(--text-tertiary);
  font-size: 2rem;
  font-weight: 300;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.skill-card {
  background: var(--bg-card);
  border-radius: 18px;
  padding: 2rem;
  text-align: center;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

html.dark .skill-card:hover {
  box-shadow: 0 20px 40px rgba(255, 255, 255, 0.05);
}

.skill-card h3 {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-primary);
  margin: 0 0 0.5rem 0;
}

.skill-card p {
  color: var(--text-tertiary);
  font-size: 1rem;
  margin: 0;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.project-card {
  background: var(--bg-card);
  border-radius: 18px;
  padding: 2rem;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

html.dark .project-card:hover {
  box-shadow: 0 20px 40px rgba(255, 255, 255, 0.05);
}

.project-card h3 {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--text-primary);
  margin: 0 0 1rem 0;
}

.project-card p {
  color: var(--text-secondary);
  line-height: 1.5;
  margin: 0 0 1.5rem 0;
}

.project-link {
  display: inline-block;
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 500;
  padding: 8px 16px;
  border-radius: 20px;
  border: 1px solid var(--accent-color);
  transition: all 0.3s ease;
}

.project-link:hover {
  background: var(--accent-color);
  color: white;
}

.contact-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.contact-link {
  display: inline-block;
  color: var(--accent-color);
  text-decoration: none;
  font-size: 1.25rem;
  font-weight: 500;
  padding: 12px 24px;
  border-radius: 24px;
  border: 2px solid var(--accent-color);
  transition: all 0.3s ease;
}

.contact-link:hover {
  background: var(--accent-color);
  color: white;
  transform: translateY(-2px);
}

.footer {
  text-align: center;
  padding: 2rem 0;
  color: var(--text-tertiary);
  font-size: 0.9rem;
}

.beian-info {
  margin-top: 1rem;
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.beian-info a {
  color: var(--text-tertiary);
  text-decoration: none;
  font-size: 0.8rem;
  transition: color 0.2s ease;
}

.beian-info a:hover {
  color: var(--text-secondary);
}

@media (max-width: 768px) {
  .hero-content .name {
    font-size: 3rem;
  }
  
  h2 {
    font-size: 2rem;
  }
  
  .skills-grid,
  .projects-grid {
    grid-template-columns: 1fr;
  }
  
  .contact-links {
    flex-direction: column;
    align-items: center;
  }
  
  section {
    padding: 60px 0;
  }
}

@media (max-width: 480px) {
  .hero-content .name {
    font-size: 2.5rem;
  }
  
  .container {
    padding: 0 16px;
  }
  
  .skill-card,
  .project-card {
    padding: 1.5rem;
  }
  
  .beian-info {
    flex-direction: column;
    gap: 0.5rem;
  }
}
</style>

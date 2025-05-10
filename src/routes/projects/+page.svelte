<script>
    import nickq from '$lib/images/AppIcon@3x.png';
    import dotdotdot from '$lib/images/AppIcon...@3x.png';
    import { onMount } from 'svelte';

    // Animation for staggered loading
    let visible = false;
    onMount(() => {
        setTimeout(() => {
            visible = true;
        }, 100);
    });
</script>

<svelte:head>
    <title>Projects | Nick Quam</title>
    <meta name="description" content="Nick Quam's Portfolio Projects" />
</svelte:head>

<div class="projects-container" class:visible>
    <h1 class="section-title">Featured Projects</h1>
    
    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <img src="{nickq}" alt="Astretto logo" class="project-logo" />
                <div class="project-title-container">
                    <h2 class="project-title">Astretto</h2>
                    <div class="project-tags">
                        <span class="tag">Social</span>
                        <span class="tag">iOS</span>
                        <span class="tag">Web</span>
                    </div>
                </div>
            </div>
            
            <p class="project-description">
                A social app where users submit a daily headline, with one getting voted on and sent to everyone each day. Connect with others through creative news-style headlines and discover trending thoughts in your community.
            </p>
            
            <div class="project-actions">
                <a href="https://www.astretto.com" target="_blank" class="button primary">Visit Website →</a>
            </div>
        </div>
    </div>
    
    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <img src="{nickq}" alt="LifeGraph logo" class="project-logo" />
                <div class="project-title-container">
                    <h2 class="project-title">LifeGraph</h2>
                    <div class="project-tags">
                        <span class="tag">Productivity</span>
                        <span class="tag">iOS</span>
                        <span class="tag">Web</span>
                    </div>
                </div>
            </div>
            
            <p class="project-description">
                A productivity application designed to help users chart and visualize their progress across various life goals and objectives. Track your growth, set milestones, and see your improvements over time with intuitive graphs and analytics.
            </p>
            
            <div class="project-actions">
                <button class="button secondary" disabled>Coming Soon</button>
            </div>
        </div>
    </div>
    
    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <img src="{nickq}" alt="nickquam.com logo" class="project-logo" />
                <div class="project-title-container">
                    <h2 class="project-title">nickquam.com</h2>
                    <div class="project-tags">
                        <span class="tag">SvelteKit</span>
                        <span class="tag">Portfolio</span>
                        <span class="tag">Web</span>
                    </div>
                </div>
            </div>
            
            <p class="project-description">
                My personal portfolio website showcasing projects and skills. Built with SvelteKit and deployed on Cloudflare Pages with GitHub integration for seamless updates.
            </p>
            
            <div class="project-actions">
                <a href="https://www.nickquam.com" target="_blank" class="button primary">Visit Website →</a>
            </div>
        </div>
    </div>
    
    <div class="project-card future-card">
        <div class="project-content">
            <div class="project-header">
                <img src="{dotdotdot}" alt="Future project" class="project-logo future-logo" />
                <div class="project-title-container">
                    <h2 class="project-title">New Project</h2>
                    <div class="project-tags">
                        <span class="tag">Coming Soon</span>
                    </div>
                </div>
            </div>
            
            <p class="project-description">
                Stay tuned for more exciting projects in development.
            </p>
        </div>
    </div>
</div>

<style>
.projects-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 1rem;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}

.projects-container.visible {
  opacity: 1;
  transform: translateY(0);
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin: 2rem 0 3rem;
  text-align: center;
  color: white;
  position: relative;
}

.project-card {
  background-color: rgba(0, 0, 0, 0.2);
  border-radius: 24px;
  margin-bottom: 2.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  overflow: hidden;
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

.project-content {
  padding: 2.5rem;
}

.project-header {
  display: flex;
  align-items: center;
  margin-bottom: 1.5rem;
}

.project-logo {
  width: 80px;
  height: 80px;
  border-radius: 16px;
  object-fit: cover;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  border: 2px solid rgba(255, 255, 255, 0.2);
  transition: transform 0.3s ease;
}

.future-logo {
  opacity: 0.6;
}

.project-title-container {
  margin-left: 1.5rem;
}

.project-title {
  font-weight: 700;
  font-size: 1.8rem;
  margin: 0 0 0.5rem;
  color: white;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 50px;
  padding: 0.25rem 0.75rem;
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--color-theme-1);
  transition: background-color 0.3s ease;
}

.project-description {
  font-size: 1.1rem;
  line-height: 1.7;
  margin-bottom: 2rem;
  color: rgba(255, 255, 255, 0.9);
}

.project-actions {
  display: flex;
  gap: 1rem;
}

.button {
  border-radius: 10px;
  padding: 0.75em 1.5em;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
}

.button.primary {
  background-color: var(--color-theme-1);
  color: white;
  border: 1px solid transparent;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.button.primary:hover {
  background-color: var(--color-theme-2);
  transform: translateY(-3px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.button.secondary {
  background-color: rgba(255, 255, 255, 0.1);
  color: white;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.button.secondary:hover {
  background-color: rgba(255, 255, 255, 0.15);
  transform: translateY(-3px);
}

.future-card {
  opacity: 0.75;
  transition: opacity 0.3s ease;
}

.future-card:hover {
  opacity: 0.9;
}

@media (max-width: 768px) {
  .project-header {
    flex-direction: column;
    text-align: center;
  }
  
  .project-logo {
    margin-bottom: 1rem;
  }
  
  .project-title-container {
    margin-left: 0;
  }
  
  .project-tags {
    justify-content: center;
  }
  
  .project-actions {
    flex-direction: column;
  }
  
  .button {
    width: 100%;
    justify-content: center;
  }
}
</style>
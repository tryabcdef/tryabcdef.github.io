---
layout: archive
title: "What I Learned Today"
permalink: /wilt/
author_profile: true
---

<style>
/* Base styles for WILT page */
.wilt-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 20px;
}

.wilt-header {
  text-align: center;
  margin-bottom: 60px;
}

.wilt-header h1 {
  font-size: 3em;
  color: #1a202c;
  margin-bottom: 15px;
  font-weight: 700;
  background: linear-gradient(120deg, #4299e1, #667eea, #4299e1);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% auto;
  animation: gradientFlow 3s linear infinite;
}

.wilt-header p {
  color: #718096;
  font-size: 1.2em;
}

@keyframes gradientFlow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.timeline {
  position: relative;
  margin: 0;
  padding: 20px 0;
}

.timeline::before {
  content: '';
  position: absolute;
  width: 3px;
  background: linear-gradient(to bottom, #4299e1, #667eea);
  top: 0;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 2px;
}

.timeline-entry {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 50px;
  position: relative;
}

.timeline-entry:nth-child(odd) {
  flex-direction: row-reverse;
}

.timeline-dot {
  width: 20px;
  height: 20px;
  background: #4299e1;
  border-radius: 50%;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  border: 4px solid white;
  box-shadow: 0 0 0 3px #4299e1;
}

.timeline-dot:hover {
  animation: pulseGlow 2s infinite;
}

@keyframes pulseGlow {
  0% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0.4); }
  70% { box-shadow: 0 0 0 10px rgba(66, 153, 225, 0); }
  100% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0); }
}

.timeline-content {
  max-width: 45%;
  background: white;
  border-radius: 15px;
  padding: 25px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.timeline-content:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}

.timeline-entry:nth-child(odd) .timeline-content {
  text-align: left;
}

.timeline-entry:nth-child(even) .timeline-content {
  text-align: right;
}

.entry-date {
  font-size: 0.9em;
  color: #4299e1;
  font-weight: 600;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.entry-section {
  margin-bottom: 15px;
  padding-left: 15px;
  border-left: 3px solid #e2e8f0;
  transition: all 0.3s ease;
}

.entry-section:hover {
  border-left-color: #4299e1;
  background: rgba(66, 153, 225, 0.05);
  padding: 10px 15px;
  border-radius: 0 8px 8px 0;
}

.archives-link {
  text-align: center;
  margin-top: 60px;
  padding: 20px;
}

.archives-link a {
  display: inline-block;
  padding: 12px 24px;
  background: linear-gradient(120deg, #4299e1, #667eea);
  background-size: 200% auto;
  color: white;
  text-decoration: none;
  border-radius: 25px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.archives-link a:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(66, 153, 225, 0.3);
  background-position: right center;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const entries = document.querySelectorAll('.timeline-entry');
  entries.forEach((entry, index) => {
    entry.style.setProperty('--animation-order', index);
  });

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        observer.unobserve(entry.target);
      }
    });
  }, {
    threshold: 0.1
  });

  entries.forEach(entry => {
    observer.observe(entry);
  });
});
</script>

<div class="wilt-container">
  <header class="wilt-header">
    <h1>What I Learned Today</h1>
    <p>Documenting daily discoveries and insights in technology and personal growth</p>
  </header>

  <div class="timeline">
    <!-- Example Timeline Entries -->
    <article class="timeline-entry">
      <div class="timeline-dot"></div>
      <div class="timeline-content">
        <div class="entry-date">12th January</div>
        <h2>AI Articles: Applications in Testing</h2>
        <p>Explored AI applications in software testing.</p>
      </div>
    </article>

    <article class="timeline-entry">
      <div class="timeline-dot"></div>
      <div class="timeline-content">
        <div class="entry-date">11th January</div>
        <h2>Ikigai: Understanding Purpose</h2>
        <p>Read and reflected on the concept of Ikigai.</p>
      </div>
    </article>
    
    <!-- Add more entries here -->
  </div>

  <div class="archives-link">
    <a href="/november-wilt">View Previous Entries</a>
  </div>
</div>

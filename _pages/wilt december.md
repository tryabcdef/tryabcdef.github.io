---
layout: archive
title: "What I Learned Today"
permalink: /wilt/
author_profile: true
---

<div class="wilt-container">
  <header class="wilt-header">
    <h1>What I Learned Today</h1>
    <p>Documenting daily discoveries and insights in technology and personal growth</p>
  </header>
  <div class="timeline">
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
  </div>
  <div class="archives-link">
    <a href="/november-wilt">View Previous Entries</a>
  </div>
</div>

<style>
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
  padding: 40px 0;
  width: 100%;
}
.timeline-entry {
  position: relative;
  margin-bottom: 60px;
  opacity: 0;
  animation: fadeIn 0.5s ease forwards;
}
@keyframes fadeIn {
  from { 
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.timeline-content {
  background: white;
  border-radius: 20px;
  padding: 30px;
  margin: 0 30px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
}
.timeline-content::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(to bottom, #4299e1, #667eea);
}
.entry-date {
  font-size: 0.9rem;
  color: #4299e1;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 15px;
  padding-left: 20px;
}
.timeline-content h2 {
  font-size: 1.8rem;
  margin-bottom: 15px;
  color: #2d3748;
  padding-left: 20px;
}
.timeline-content p {
  color: #4a5568;
  line-height: 1.8;
  padding-left: 20px;
}
.timeline-content:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 20px 40px rgba(66, 153, 225, 0.2);
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
.timeline-connector {
  position: absolute;
  border: 3px solid #4299e1;
  border-radius: 0 0 0 50px;
  width: 50%;
  height: 100px;
  top: 50%;
  right: -30px;
  border-right: 0;
  border-top: 0;
  z-index: 1;
}
.timeline-dot {
  width: 20px;
  height: 20px;
  background: white;
  border: 4px solid #4299e1;
  border-radius: 50%;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 2;
}
.timeline-entry:nth-child(odd) .timeline-dot {
  right: -10px;
}
.timeline-entry:nth-child(even) .timeline-dot {
  left: -10px;
}
.timeline-entry::before {
  display: none;
}
/* Staggered animation delay for entries */
.timeline-entry:nth-child(1) { animation-delay: 0.1s; }
.timeline-entry:nth-child(2) { animation-delay: 0.3s; }
.timeline-entry:nth-child(3) { animation-delay: 0.5s; }

/* Position boxes */
.timeline-entry:nth-child(odd) {
  justify-content: flex-end;
}

.timeline-entry:nth-child(even) {
  justify-content: flex-start;
}
</style>
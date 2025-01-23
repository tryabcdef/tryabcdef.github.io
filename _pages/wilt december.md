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
  padding: 20px 0;
  width: 100%;
}
.timeline::before {
  content: '';
  position: absolute;
  width: 3px;
  height: calc(100% - 50px);
  background: #4299e1;
  left: 50%;
  top: 50px;
}
.timeline-entry {
  position: relative;
  margin-bottom: 80px;
  display: flex;
  width: 100%;
}
.timeline-entry:nth-child(odd) {
  justify-content: flex-end;
}
.timeline-entry:nth-child(even) {
  justify-content: flex-start;
}
.timeline-entry::before {
  content: '';
  position: absolute;
  background: #4299e1;
  z-index: 1;
}
.timeline-entry:nth-child(odd)::before {
  width: 50px;
  height: 50px;
  right: 80%;
  top: 10px;
  border: 3px solid #4299e1;
  border-left: 0;
  border-bottom: 0;
  border-radius: 0 50px 0 0;
  background: transparent;
}
.timeline-entry:nth-child(even)::before {
  width: 50px;
  height: 50px;
  left: 80%;
  top: 10px;
  border: 3px solid #4299e1;
  border-right: 0;
  border-bottom: 0;
  border-radius: 50px 0 0 0;
  background: transparent;
}
.timeline-entry:nth-child(even)::after {
  display: none;
}
.timeline-dot {
  width: 20px;
  height: 20px;
  background: #4299e1;
  border-radius: 50%;
  z-index: 2;
  border: 4px solid white;
  box-shadow: 0 0 0 3px #4299e1;
  position: absolute;
  top: 10px;
}
.timeline-entry:nth-child(odd) .timeline-dot {
  right: 80%;
  transform: translateX(50%);
}
.timeline-entry:nth-child(even) .timeline-dot {
  left: 80%;
  transform: translateX(-50%);
}
.timeline-entry:nth-child(odd) .timeline-content {
  margin-right: 40px;
}
.timeline-entry:nth-child(even) .timeline-content {
  margin-left: 40px;
}
.timeline-content {
  width: 80%;
  background: white;
  border-radius: 15px;
  padding: 25px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  z-index: 2;
}
.timeline-content:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}
.entry-date {
  font-size: 0.9em;
  color: #4299e1;
  font-weight: 600;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
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
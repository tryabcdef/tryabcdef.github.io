---
layout: archive
title: "Work experience"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<style>
/* Ensure our styles work with the archive layout */
.archive {
    padding-right: 0;
}

.experience-container {
    width: 100%;
    max-width: 100%;
    padding: 0 20px;
}

.timeline {
    position: relative;
    padding: 20px 0;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 25px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: #2196F3;
}

.experience-card {
    position: relative;
    margin: 30px 0 30px 55px;
    padding: 25px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 3px 8px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
    border: 1px solid #eaeaea;
}

.experience-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.experience-card::before {
    content: '';
    position: absolute;
    left: -42px;
    top: 25px;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background: #fff;
    border: 3px solid #2196F3;
    box-shadow: 0 0 0 3px rgba(33, 150, 243, 0.2);
}

.job-title {
    font-size: 1.25em;
    color: #1976D2;
    margin: 0 0 8px 0;
    font-weight: 600;
    line-height: 1.3;
}

.company {
    color: #666;
    font-size: 0.95em;
    margin-bottom: 15px;
    display: block;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
}

.duties {
    list-style: none;
    padding: 0;
    margin: 0;
}

.duties li {
    margin-bottom: 10px;
    padding-left: 20px;
    position: relative;
    line-height: 1.6;
}

.duties li::before {
    content: '•';
    color: #2196F3;
    position: absolute;
    left: 0;
    font-weight: bold;
}

.skills-section {
    margin-top: 50px;
    background: #f8f9fa;
    padding: 30px;
    border-radius: 8px;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    margin-top: 25px;
}

.skill-category {
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.skill-category h3 {
    color: #1976D2;
    margin: 0 0 15px 0;
    padding-bottom: 10px;
    border-bottom: 2px solid #e0e0e0;
    font-size: 1.1em;
}

.skill-category ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.skill-category li {
    margin-bottom: 8px;
    padding-left: 20px;
    position: relative;
}

.skill-category li::before {
    content: '→';
    color: #2196F3;
    position: absolute;
    left: 0;
}

.education-section {
    margin-top: 50px;
    padding: 30px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
    border: 1px solid #eaeaea;
}

.education-section h2 {
    color: #1976D2;
    margin: 0 0 20px 0;
    padding-bottom: 10px;
    border-bottom: 2px solid #e0e0e0;
}

.education-section ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.education-section li {
    margin-bottom: 12px;
    padding-left: 25px;
    position: relative;
}

.education-section li::before {
    content: '🎓';
    position: absolute;
    left: 0;
}

.download-button {
    display: inline-block;
    margin-top: 40px;
    padding: 12px 28px;
    background: #2196F3;
    color: white;
    text-decoration: none;
    border-radius: 6px;
    transition: all 0.3s ease;
    font-weight: 500;
    border: none;
    box-shadow: 0 2px 4px rgba(33, 150, 243, 0.2);
}

.download-button:hover {
    background: #1976D2;
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(33, 150, 243, 0.3);
}

/* Responsive adjustments */
@media screen and (max-width: 768px) {
    .experience-container {
        padding: 0 15px;
    }
    
    .experience-card {
        margin-left: 45px;
        padding: 20px;
    }
    
    .timeline::before {
        left: 20px;
    }
    
    .experience-card::before {
        left: -37px;
    }
    
    .skills-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="experience-container">
    <div class="timeline">
        <div class="experience-card">
            <div class="job-title">SDET (Software Development Engineer in Test)</div>
            <div class="company">Skeps (Jun. 2024 - Present)</div>
            <ul class="duties">
                <li>Conduct grey-box and white-box testing, reviewing code and developer pull requests for accuracy.</li>
                <li>Deployed builds via Jenkins in CI/CD pipelines, optimizing test coverage and system efficiency.</li>
                <li>Performed API and webhook testing to validate system functionalities, ensuring seamless loan facilitation.</li>
            </ul>
        </div>

        <div class="experience-card">
            <div class="job-title">Analyst</div>
            <div class="company">Studiographene (Mar. 2023 - Jun. 2024)</div>
            <ul class="duties">
                <li>Contributed to creating of test plans, test cases, and defect reports, streamlining the QA process.</li>
                <li>Executed functional, API, and regression testing for web and mobile applications to ensure quality standards.</li>
                <li>Monitored and reported quality KPIs, providing actionable insights to stakeholders.</li>
            </ul>
        </div>

        <div class="experience-card">
            <div class="job-title">Associate Quality Analyst</div>
            <div class="company">Copper Mobile Pvt. Ltd. (Dec. 2021 - Feb. 2023)</div>
            <ul class="duties">
                <li>Developed and executed test cases for cross-platform mobile and web applications.</li>
                <li>Managed bug defect reports in JIRA and collaborated with developers to resolve issues efficiently.</li>
                <li>Presented testing outcomes in client demos and integrated feedback to enhance product quality.</li>
            </ul>
        </div>

        <div class="experience-card">
            <div class="job-title">Associate Quality Analyst Trainee</div>
            <div class="company">Copper Mobile Pvt. Ltd. (Sept. 2021 - Dec. 2021)</div>
            <ul class="duties">
                <li>Created and executed test cases.</li>
                <li>Conducted sanity, functional, and regression testing on web and mobile applications.</li>
                <li>Performed API testing using Postman and Swagger.</li>
            </ul>
        </div>
    </div>

    <div class="skills-section">
        <h2>Skills</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>Technical Skills</h3>
                <ul>
                    <li>UI Automation Testing</li>
                    <li>Functional & API Testing</li>
                    <li>White Box Testing</li>
                    <li>Accessibility Testing</li>
                </ul>
            </div>
            
            <div class="skill-category">
                <h3>Soft Skills</h3>
                <ul>
                    <li>Critical Thinking</li>
                    <li>Client Handling</li>
                    <li>QA Documentation</li>
                </ul>
            </div>
            
            <div class="skill-category">
                <h3>Tools & Frameworks</h3>
                <ul>
                    <li>Selenium, Pytest, BDD</li>
                    <li>Python</li>
                    <li>Git, Jenkins & Docker</li>
                    <li>Katalon, Postbot</li>
                    <li>Chat-GPT, Co-Pilot, Claude</li>
                </ul>
            </div>
        </div>
    </div>

    <div class="education-section">
        <h2>Education</h2>
        <ul>
            <li>B.Tech. (Hons.) in Computer Science Engineering, 2017</li>
            <li>M.S. in Mathematics, Veer Bahadur Singh Purvanchal University, 2020</li>
            <li>ISTQB CTFL Certification, July 2023</li>
        </ul>
    </div>

    <a href="/files/Ujjwal_Kumar_Singh_3_Years_Experience_QA_Resume.pdf" class="download-button" download>
        Download Resume
    </a>
</div>
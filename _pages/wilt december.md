---
layout: archive
title: "What I Learned Today"
permalink: /wilt/
author_profile: true
---

<style>
/* Base styles from previous design */
.wilt-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 20px;
}

@keyframes gradientFlow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes scaleIn {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-100px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(100px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes pulseGlow {
  0% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0.4); }
  70% { box-shadow: 0 0 0 10px rgba(66, 153, 225, 0); }
  100% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0); }
}

.wilt-header {
  text-align: center;
  margin-bottom: 60px;
  position: relative;
  opacity: 0;
  animation: fadeInUp 0.8s ease forwards;
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

.timeline {
  position: relative;
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
  animation: scaleIn 1s ease forwards;
}

.timeline-entry {
  width: 100%;
  margin-bottom: 50px;
  position: relative;
  opacity: 0;
}

.timeline-entry:nth-child(odd) {
  padding-right: calc(50% + 30px);
  animation: slideInLeft 0.8s ease forwards;
  animation-delay: calc(var(--animation-order) * 0.2s);
}

.timeline-entry:nth-child(even) {
  padding-left: calc(50% + 30px);
  animation: slideInRight 0.8s ease forwards;
  animation-delay: calc(var(--animation-order) * 0.2s);
}

.timeline-content {
  background: white;
  border-radius: 15px;
  padding: 25px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: relative;
  transition: all 0.3s ease;
}

.timeline-content:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}

.timeline-dot {
  width: 20px;
  height: 20px;
  background: #4299e1;
  border-radius: 50%;
  position: absolute;
  top: 20px;
  left: 50%;
  transform: translateX(-50%) scale(0);
  z-index: 2;
  border: 4px solid white;
  box-shadow: 0 0 0 3px #4299e1;
  animation: scaleIn 0.5s ease forwards;
  animation-delay: calc(var(--animation-order) * 0.2s + 0.3s);
}

.timeline-dot:hover {
  animation: pulseGlow 2s infinite;
}

.entry-date {
  font-size: 0.9em;
  color: #4299e1;
  font-weight: 600;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
  opacity: 0;
  animation: fadeInUp 0.5s ease forwards;
  animation-delay: calc(var(--animation-order) * 0.2s + 0.4s);
}

.entry-section {
  margin-bottom: 15px;
  padding-left: 15px;
  border-left: 3px solid #e2e8f0;
  transition: all 0.3s ease;
  opacity: 0;
  animation: fadeInUp 0.5s ease forwards;
  animation-delay: calc(var(--animation-order) * 0.2s + 0.5s);
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
  opacity: 0;
  animation: fadeInUp 0.8s ease forwards;
  animation-delay: 1s;
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

  // Add intersection observer for animation triggers
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
    <p>Documenting daily discoveries and insights in technology and personal growth</p>
  </header>

   <div class="timeline">
    <!-- January 12 -->
    <article class="timeline-entry">
      <div class="timeline-dot"></div>
      <div class="timeline-content">
        <div class="entry-date">12th January</div>
        <h2 class="entry-title">AI Articles: Applications in Testing</h2>
        
        <div class="entry-section">
          <div class="section-title">Learning</div>
          <div class="section-content">Explored AI applications in software testing.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Description</div>
          <div class="section-content">I read several online articles about the emerging role of AI in software testing, particularly how it can help in automating test case generation, bug detection, and even predicting potential issues based on historical data.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Key Takeaway</div>
          <div class="section-content">AI can revolutionize the testing process by reducing manual efforts and improving test coverage. Its ability to predict defects and automate repetitive tasks offers a significant efficiency boost.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Personal Reflection</div>
          <div class="section-content">I'm excited about the possibilities of AI in testing. It could drastically improve how we approach quality assurance in the future, and I'm eager to explore this further.</div>
        </div>
      </div>
    </article>

    <!-- January 11 -->
    <article class="timeline-entry">
      <div class="timeline-dot"></div>
      <div class="timeline-content">
        <div class="entry-date">11th January</div>
        <h2 class="entry-title">Ikigai: Understanding Purpose</h2>
        
        <div class="entry-section">
          <div class="section-title">Learning</div>
          <div class="section-content">Read and reflected on the concept of Ikigai.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Description</div>
          <div class="section-content">I continued reading Ikigai and explored how it promotes finding balance in life by focusing on four pillars: what you love, what you're good at, what the world needs, and what you can be paid for.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Key Takeaway</div>
          <div class="section-content">Ikigai offers a holistic approach to achieving happiness and fulfillment by aligning your passions, talents, societal needs, and financial success.</div>
        </div>

        <div class="entry-section">
          <div class="section-title">Personal Reflection</div>
          <div class="section-content">This book has made me think about how I can better align my work and personal life with my values and purpose. It's a powerful perspective for overall well-being.</div>
        </div>
      </div>
    </article>

<!-- January 10 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">10th January</div>
    <h2 class="entry-title">Pytest: Test Reporting</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Learned how to generate detailed test reports in pytest.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I explored generating reports using pytest's built-in features and plugins. This is essential for tracking the results of automated UI tests, especially when running large test suites.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Having test reports that detail pass/fail statuses, along with error traces, makes debugging and tracking test progress much easier. It helps in maintaining transparency within the team.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I've come to realize that reporting is just as important as running the tests themselves. It's a great way to communicate results clearly to stakeholders.</div>
    </div>
  </div>
</article>

<!-- January 9 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">9th January</div>
    <h2 class="entry-title">Pytest and Selenium Integration</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Integrated pytest with Selenium for UI tests.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I successfully integrated pytest with Selenium to run automated UI tests. This allowed me to run multiple test cases with a single pytest command, managing different test scenarios more efficiently.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Integrating pytest with Selenium helps streamline testing by leveraging pytest's advanced features like fixtures and reporting, making it ideal for UI testing.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">Seeing pytest and Selenium work together smoothly was rewarding. I now have a more organized testing environment, which will save time in the long run.</div>
    </div>
  </div>
</article>

<!-- January 8 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">8th January</div>
    <h2 class="entry-title">Selenium: Browser Navigation and Assertions</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Explored browser navigation and assertions in Selenium.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I worked on automating browser navigation tasks, like going back, forward, refreshing, and handling windows or tabs. Additionally, I practiced making assertions to verify page titles, URLs, and element visibility.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Navigating between pages and validating the page state with assertions are fundamental aspects of UI Automation testing, ensuring that tests reflect the intended behavior of the application.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I appreciate how Selenium allows for precise control of browser behavior. I'm starting to feel more confident in my ability to automate complex workflows.</div>
    </div>
  </div>
</article>

<!-- January 7 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">7th January</div>
    <h2 class="entry-title">Selenium: Handling Waits</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Learned about handling waits in Selenium.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I explored the different types of waits in Selenium: implicit, explicit, and fluent waits. Each type helps in managing synchronization issues between the browser's actions and the script's execution.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Managing waits properly is crucial for ensuring that automation scripts run smoothly without errors due to page loading times or dynamic content.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">This was an important topic, as I've encountered issues in previous projects due to improper waits. Now, I have the tools to fix those issues and improve test reliability.</div>
    </div>
  </div>
</article>

<!-- January 6 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">6th January</div>
    <h2 class="entry-title">Selenium: Locators and Element Interaction</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Explored how to locate elements and interact with them in Selenium.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I delved into different strategies for locating web elements, such as using ID, name, class name, XPath, and CSS selectors. I also practiced performing actions like clicking, typing, and selecting items from dropdowns.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Understanding how to effectively locate and interact with web elements is key to automating real-world UI tasks. Different locator strategies offer flexibility in dealing with complex web pages.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I'm getting better at identifying the most efficient way to locate elements, which will make my tests faster and more reliable in the long run.</div>
    </div>
  </div>
</article>

<!-- January 5 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">5th January</div>
    <h2 class="entry-title">Selenium: Webdriver Basics</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Learned about Selenium WebDriver basics.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I explored the functionality of Selenium WebDriver, including how to launch browsers, navigate between pages, and interact with web elements. I practiced automating some basic tasks like clicking buttons and filling out forms.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">WebDriver is the heart of Selenium automation, and mastering its basic functions is essential for any UI Automation project. It provides a powerful interface for controlling web browsers.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I enjoy how easy it is to automate repetitive tasks with WebDriver. I can see this speeding up the testing and quality assurance process.</div>
    </div>
  </div>
</article>

<!-- January 4 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">4th January</div>
    <h2 class="entry-title">UI Automation Project: Selenium Setup</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Set up my Selenium-based UI Automation project.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I started configuring the environment for my UI Automation project using Selenium with Python. This involved setting up the necessary dependencies, creating test scripts for basic browser actions like opening a page and interacting with elements.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Proper setup of Selenium and its integration with Python is crucial for smooth automation. Understanding how to configure the environment correctly makes future developments easier.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">It was fulfilling to see my initial setup work. I'm excited to build on this foundation and automate more complex interactions with web elements.</div>
    </div>
  </div>
</article>

<!-- January 3 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">3rd January</div>
    <h2 class="entry-title">Pytest Framework: Utilities</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Explored utilities in the pytest framework.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I focused on understanding pytest's utility functions, like pytest.mark.parametrize, which helps in running tests with multiple sets of inputs. I also explored custom utility functions to help with test setups and assertions.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Utilizing pytest's built-in utilities like parametrize can significantly reduce the amount of code in tests and improve coverage. Custom utilities can further enhance the efficiency of test scripts.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I find it useful to abstract repetitive logic into utility functions. It's a great way to simplify tests and maintain clean code.</div>
    </div>
  </div>
</article>

<!-- January 2 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">2nd January</div>
    <h2 class="entry-title">Pytest Framework: conftest.py</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Worked with conftest.py in pytest.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I explored how to use conftest.py for sharing fixtures, hooks, and other configurations across multiple test files. This setup allows for cleaner and more reusable code, reducing redundancy in test scripts.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">conftest.py is a central file in pytest that helps in organizing fixtures and configurations. By using it, I can make my tests more modular and reusable.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I can see how this feature will make my test suites more scalable. It's great for maintaining consistency across tests while reducing duplication.</div>
    </div>
  </div>
</article>

<!-- January 1 -->
<article class="timeline-entry">
  <div class="timeline-dot"></div>
  <div class="timeline-content">
    <div class="entry-date">1st January</div>
    <h2 class="entry-title">Pytest Framework: Logging</h2>
    
    <div class="entry-section">
      <div class="section-title">Learning</div>
      <div class="section-content">Explored the logging feature in the pytest framework.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Description</div>
      <div class="section-content">I learned how logging works in pytest to capture detailed information about test execution, which is useful for debugging and understanding test behavior. By setting up a basic logging configuration, I was able to track events, errors, and other useful information during test runs.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Key Takeaway</div>
      <div class="section-content">Logging in pytest helps identify the root cause of test failures and improves the visibility of test execution. It is essential for debugging and improving the reliability of test automation.</div>
    </div>

    <div class="entry-section">
      <div class="section-title">Personal Reflection</div>
      <div class="section-content">I realized how powerful logging is in making tests more transparent. It’s something I can implement more in my testing workflows to troubleshoot issues faster.</div>
 </div>
  </div>
</article>
    <!-- Archive Link -->
    <div class="archives-link">
      <a href="/november-wilt">View Previous Entries</a>
    </div>
  </div>
</div>
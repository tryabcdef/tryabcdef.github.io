---
title: "When single alphabet decided the fate of the first demo"
collection: testing-musings
type: "Deployment"
permalink: /testing-musings/importance-of-single-alphabet
venue: "Bug"
date: 2024-10-10
location: "City"
---

**Everything that happens the first time is special because of its first-time experience.**




It was mid-December in 2021, and my internship was still going on, I was testing a mobile application for a project that was intended to be an in-company notification app to provide notifications related to companies to all the employees of the companies. Although this was my second project during the internship, it holds a special place for me. Even though the app had limited functionality from the learning point of view it offered lot of things to learn.  

The app was developed for Android and iOS separately, so the testing strategies for testing the app on both platforms were different. After a month of development, the first demo of the project was scheduled for Friday evening. So now, as the date was finalized and approaching, the team was in full swing to complete the pending task, as the first MVP for delivery was planned after the delivery.  


Testing Challenges
======

As the primary goal of the app was to provide notifications We tested push notifications in every possible scenario to ensure a seamless experience for the user. However, during the testing phase, we faced many challenges, especially in Android devices for the UI. Differences in screen sizes between Android devices (5.5–6+ inches) caused minor UI inconsistencies, which we addressed. Another challenge was that we were using 3rd party API for notification and as the API was mostly designed for the customer of the USA their server would remain down during office time IST which made it challenging some time to test the app during office hours.   


Demo Started
======

On the day of the demo, we did our final round of sanity testing to ensure the build was stable and there was no technical glitch from our side. As it was the first demo for me as a software tester there was some nervousness in the atmosphere. So the demo started at 9PM (IST) and as it was mid-December winter had started and the majority of the office employees had left the office. Only a couple of people were in the office including me, the delivery manager, and a few other people.  

We expected a small group from the client side, but to our surprise, 13 people joined the meeting, including their creative director. Their presence added to my jitters. Everything was going smoothly until someone from their creative team interrupted, pointing out a discrepancy in the text 'Notifications' on Android versus 'Notification' on iOS. Suddenly, all eyes were on this minor yet significant inconsistency.


Build Rejected
======
The moment one of the members pointed out the difference between "Notification" and "Notifications," it quickly became the center of attention. Soon, everyone began discussing how the text not only looked inconsistent but also conveyed different meanings. After an extensive discussion, the client decided to reject the builds, requesting immediate fixes before scheduling another delivery.

Initially, I had high hopes for the demo, given the app's performance and stability during testing. However, the rejection of the build during my first demo was an outcome I hadn't anticipated. What I thought would be a smooth first-time experience became an eye-opening moment, fundamentally reshaping my approach to testing strategies.


Lessons Learned
=====

* <b>Importance of UI/UX Testing: </b> Even though functional testing has its own importance the experience from the first demo was enough to teach me the importance of UI/UX Testing.  

* <b>Feedback of Non-Technical Stakeholders: </b> While we usually talk about the primary stakeholders who are involved in the project there are non-technical stakeholders whose feedback is also very helpful in enhancing the app user interface. 

* <b>Being confident is better than being nervous:</b> While testing the product it is important to have faith in our testing strategies as well as in the product that we are aiming to deliver,Showing nervousness to stakeholders may bring question in their mind regarding the stability of the product.
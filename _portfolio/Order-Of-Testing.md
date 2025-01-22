---
title: "Order Of Testing"
excerpt: "Order Of Testing To Be Followed On New Releases."
collection: testing-mindspace
---

When a new build is released by developing team for testing, the testing should be performed in certain order 

<img src='/images/order-of-testing.jpg'>


* <b>Smoke Testing
* Purpose: Smoke testing is a preliminary check to ensure that the basic functionalities of the build are working and that the build is stable enough for further testing.
* Process:
    * Test critical paths like application launch, login functionality, or core features.
    * Identify if the build is broken or unstable.
* Outcome: If the build passes smoke testing, it proceeds to the next phase. If it fails, the build is rejected and sent back to the development team for fixes.

* <b>2. Sanity Testing
* Purpose: Sanity testing verifies that the new code changes or bug fixes have not affected the existing functionality of the application.
* Process:
    * Perform focused tests on the areas that have undergone changes.
    * Check if the bug fixes work as intended.
* Outcome: If sanity tests pass, it ensures that critical functionality is intact, and the build can move on to more detailed testing.

* <b>3. Functional Testing
* Purpose: Functional testing ensures that all the features of the application work according to the specified requirements.
* Process:
    * Create and execute test cases based on the functional requirements.
    * Validate inputs, actions, and expected outputs.
* Outcome: Detects functional defects in the system, ensuring that the application behaves as expected.

* <b>4. System Testing
* Purpose: System testing verifies that the entire application works together as a cohesive system.
* Process:
    * Test the interaction between different modules.
    * Check end-to-end scenarios that reflect real-world usage.
* Outcome: Ensures that the system meets the specified requirements and works as a whole.

* <b>5. Retesting
* Purpose: Retesting is focused on verifying that previously reported bugs have been fixed correctly.
* Process:
    * Re-execute the failed test cases from the previous build after the defects have been fixed.
    * Ensure no new issues are introduced in the process.
* Outcome: Confirms that the fixes work correctly without affecting existing functionalities.

* <b>6. Regression Testing
* Purpose: Regression testing ensures that recent code changes have not introduced new bugs in the unchanged parts of the software.
* Process:
    * Re-run previously executed test cases to verify that existing functionalities still work as expected.
    * Utilize automation if possible for repetitive test cases.
* Outcome: Ensures that old code works perfectly even after new changes or fixes are implemented.

* <b>7. Sanity Testing on UAT (User Acceptance Testing) Environment
* Purpose: This is a final check in the UAT environment to ensure the build is ready for end-user testing or deployment.
* Process:
    * Perform critical checks similar to the earlier sanity test but now in the UAT environment.
    * Ensure that all functionalities are intact and meet the user expectations.
* Outcome: Ensures the build is deployment-ready, and any critical issues are resolved.

* <b>8. Deployment on Production
* Purpose: The goal here is to deploy the build into the live environment.
* Process:
    * Ensure the build is successfully deployed with no errors in the production environment.
    * Validate the deployment process by monitoring logs and deployment metrics.
* Outcome: The application is deployed, and it is now accessible to end users.

* <b>9. Smoke Testing on Production
* Purpose: Perform smoke testing in the production environment to ensure that the deployment did not break any core functionalities.
* Process:
    * Execute essential tests like logging in, navigating the key paths, or performing critical actions.
* Outcome: Ensures the system is stable and ready for real-world use by customers without critical issues.


The order of testing may vary from team to team or organization to organization. However, at the end of the day, regardless of the order followed, the ultimate goal should always be to ensure that the quality meets the business requirements.

In addition to the outlined testing types, teams can also incorporate other approaches, such as:

* <b>Exploratory Testing :</b>  Exploratory testing involves simultaneously learning, designing, and executing tests. It allows testers to uncover unexpected issues by exploring the application without predefined scripts. This approach is particularly valuable for identifying edge cases and usability concerns that may be missed in scripted testing.
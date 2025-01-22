---
title: "How To Test Login Page On Web Application"
excerpt: "Mind-Map showcasing how to test login feature on Web Application"
collection: testing-mindspace
---

<b>When testing a login page with email, password, and "Remember Me" fields, there are multiple positive and negative test cases that can be explored: </b>

<img src='/images/login-test.jpeg'>


* <b>1. UI Testing</b>
* UI of the Login Page: Verify that the entire login page is visible and correctly displayed, including the logo, input fields, buttons, and any other UI elements.
* Possible Combinations: Test on different browsers (Chrome, Firefox, Safari, etc.) and devices (desktop, mobile, tablet) to ensure responsiveness.
* UI of Input Fields: Ensure all input fields (email, password) have proper placeholders and are clearly visible.
Possible Combinations: Check for correct alignment, font size, and color contrast.

* <b>2. UX Testing</b>
* Time to Load the Entire Page: Measure the time taken for the login page to load all its content.
* Possible Combinations: Test on different network speeds (3G, 4G, Wi-Fi) and simulate slow connections.
* Time to Submit the Application: Check the time it takes from clicking "Login" to receiving a response (success or error).
* Possible Combinations: Test under heavy server load or simulate high-latency conditions.

* <b>3. Email Field Testing</b>
* Valid Email: Enter valid email formats (e.g., user@example.com) and ensure proper acceptance.

* Possible Combinations:</b>
    * Registered vs. unregistered email.
    * Verify case-insensitivity (upper/lowercase combinations).
    * Invalid Email: Test various invalid formats.
    * Without .com (e.g., user@domain)
    * Missing @ symbol (e.g., userdomain.com)
    * Incomplete email (e.g., user@)
    * Email in Different Cases: Test email with variations in letter case:
    * First letter capitalized (User@example.com)
    * All letters capitalized (USER@EXAMPLE.COM)
    * Random capitalization (uSeR@eXaMpLe.cOm)
    * Without Email: Submit the form without entering an email and verify the appropriate error message.
    * Expected Behavior: Display error like “Email is required.”

* <b>4. Password Field Testing</b>
* Valid Password: Enter a correct password that meets the application’s criteria.
* Invalid Password
* Wrong password.
* Password with incorrect combinations (e.g., symbols instead of letters).
* Blank Password: Attempt to submit without entering a password.
* Expected Behavior: Display error like “Password is required.”
* Identify Drop-off Points: Track user behavior to identify where they abandon the login process.

* <b>5. Remember Me Field Testing</b>
* Tick Remember Me Checkbox on First Login: Ensure the session persists even after closing the browser.
* Tick Remember Me Checkbox on Next Login: Ensure the email/password fields are pre-filled or remembered.
* Login Without Ticking Remember Me: Ensure login credentials are not stored.
* Untick Remember Me After Previous Tick: Ensure unticking does not save credentials.

* <b>6. Functionality Testing</b>
* Login with Valid Email & Valid Password: Successful login expected.
* Login with Valid Email & Invalid Password: Display error like “Incorrect password.”
* Login with Invalid Email & Valid Password: Display error like “Invalid email format.”
* Login with Email & No Password: Expect “Password is required.”
* Login Without Email & With Password: Expect “Email is required.”
* Login Without Email & Without Password: Expect both error messages.
* Login with Remember Me Checked: Verify persistence across sessions.
* Login with Different Case Email: Verify case-insensitivity.
* Login with Capitalized Password: Ensure passwords are case-sensitive if required.

* <b>Additional Combinations:</b>
* Brute Force Prevention: Ensure login attempts are blocked after several failed attempts.
* Session Timeout: Verify that inactive sessions expire after a set time.
* Password Reset Link: Test if the “Forgot Password” link redirects to the appropriate flow.
* Captcha Integration: Check if CAPTCHA prevents automated login attempts.
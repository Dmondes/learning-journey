This repo documents my learning journey as I study and practice software testing, focusing on both **manual** and **automation** testing.
The goal: to clearly understand each concept, write notes in my own words, and track progress.

Concept 1: The Fundamental Role (The "Checker")
Core Idea: Software development has two main roles: the Maker (Developer) who builds the product, and the Checker (Tester/QA) who verifies it works as expected before it reaches customers. The goal is to ensure quality and find problems (bugs or defects).
Key Term:
Quality Assurance (QA): The entire process of ensuring a high-quality product.
Check Your Understanding
Mentor's Question: In your own words, what is the main goal of a software tester? What is the difference between a developer and a tester?
My Refined Answer: The goal is to ensure the software can accomplish what it is set up to do. The difference is being the maker vs. the checker.
Concept 2: The Two Methods of Testing
Core Idea: There are two ways to "check" the software. This job requires both.
Manual Testing: A human physically interacts with the software (clicking buttons, typing text) to find bugs. This is essential for testing things that require human judgment, like aesthetics or ease-of-use.
Automation Testing: A person writes a program (script) to test the software automatically. This is perfect for tasks that are repetitive, predictable, and need to be run often.
Key Terms:
UI/UX (User Interface/User Experience): How the software looks and feels to a human user. Best tested manually.
Regression Testing: Re-running old tests to make sure that new changes haven't broken existing features. This is the most common use for automation.
Check Your Understanding
Mentor's Question: A developer changes a website's login page.
How do you check that the "Login" button still works?
How do you check that the new design looks good and isn't confusing?
My Refined Answer:
I would run the automated Regression Test suite to check existing functionality.
I would perform manual UI testing to validate the user experience.
Concept 3: The Automation Toolbox
Core Idea: To build an automation "robot," you need two things: a language and a toolkit.
Programming Language (e.g., Python, Java): The language you use to write the step-by-step instructions (the script).
Automation Framework (e.g., Selenium, Appium): A pre-built toolkit of commands and functions that makes it easier to interact with the application.
Key Frameworks:
Selenium: The industry standard for automating web browsers.
Appium: The industry standard for automating mobile applications.
Check Your Understanding
Mentor's Question: You need to write a test that automatically logs into Yokogawa's company website.
Which framework would you use? Why?
What is the role of the programming language in this task?
My Refined Answer:
I would use Selenium, as it is the framework specifically designed for testing websites.
The programming language (like Python) is used to write the actual instructions, telling Selenium what to do, such as "find the username field" and "click the login button."
Concept 4: The Testing Process (Plan -> Find -> Report)
Core Idea: Testing is a structured process, like a detective's investigation.
Plan: Create a Test Plan (overall strategy) and write detailed, step-by-step Test Cases that define what to test and the expected outcome.
Find: Execute the test cases. If the actual result doesn't match the expected result, you've found a bug.
Report: Document the bug in a Bug Report so developers can find and fix it.
Key Tool:
JIRA: A project management tool used to track tasks, create bug reports, and manage the workflow.
Check Your Understanding
Mentor's Question: You're testing a shopping site. Your test case says clicking "Add to Cart" should change the cart icon to "1". You click it, but the icon still shows "0". What do you do?
My Refined Answer:
I have found a bug (or software defect).
My next step is to raise a ticket in JIRA. I would give it a clear title ("Cart icon not updated when item is added"), provide the exact steps to reproduce it, and state the expected vs. actual result. I would also set its severity, assign it to the correct development team, and attach it to the relevant project.
Concept 5: The Team's Rhythm (Agile/Scrum)
Core Idea: Modern software teams work in a collaborative rhythm called Agile. The most popular Agile framework is Scrum.
Instead of building the entire product at once (Waterfall), the team works in short cycles called Sprints (usually 2 weeks).
In each sprint, the team builds a small number of features completely.
The tester is involved from the very beginning of the sprint, providing continuous feedback to developers, which makes fixing bugs much faster and cheaper.
Check Your Understanding
Mentor's Question: What is the biggest advantage for a tester being involved throughout a sprint instead of just waiting at the end?
My Refined Answer: The biggest advantage is providing continuous feedback. This allows developers to fix bugs when they are small and simple, rather than waiting until the end when they are complex and costly to fix. It also allows me, the tester, to maintain a steady, predictable workload.
Concept 6: Advanced Tools (Testing the "Invisible")
Core Idea: Not all software is visible. We need special tools to test the "back-end" or performance under pressure.
API Testing: An API is the messenger between the user interface (front-end) and the server (back-end). Tools like Postman and RestAssured allow you to test the API directly, without using the user interface.
Performance/Load Testing: This tests the system's stability and speed when many users access it at the same time. Tools like JMeter and LoadRunner simulate this heavy "load."
Check Your Understanding
Mentor's Question: For a new mobile banking app:
How would you test the back-end function for fetching a bank balance before the app screen is built?
How would you ensure the app won't crash when 50,000 users log in on payday?
My Refined Answer:
I would use an API testing tool like Postman. I would make a GET request to the specific API endpoint and verify that the response status is 200 and that the correct balance is shown in the response payload.
This requires performance testing. I would use a tool like JMeter to simulate the load of 50,000 virtual users logging in simultaneously to identify performance bottlenecks.
Concept 7: The "What" - Yokogawa's Products
Core Idea: Based on the tools in the job description (Selenium, Appium, Postman), the role is likely focused on the modern software layers that connect to Yokogawa's core industrial systems.
Layer 1: Core Control (DCS/SIS): The deep, embedded systems. (Less likely for this role).
Layer 2: Plant Operations Layer: Software with web dashboards (HMI), reporting tools, and databases that visualize plant data. (A very likely candidate).
Layer 3: Advanced Analytics & Cloud Layer: Modern platforms using IoT, AI, and Digital Twins for predictive maintenance and optimization. (Also a very likely candidate).
Putting It All Together: Answering the Big Question
Mentor's Question: In the interview, if they ask you, "What do you think you'll be testing here?", how would you answer?
My Polished Answer: "From my understanding of Yokogawa's business and the tools listed in the description, I believe the role is focused on the software layers that sit on top of the core control systems. I would expect to be testing applications like your OpreX operational dashboards or perhaps your asset management platforms. My role would likely involve using Selenium to ensure the web-based HMI is intuitive and functions correctly for plant engineers, while also using tools like Postman to verify the integrity of the real-time data being passed from the back-end servers through the APIs."

<p align="center">
    <img src="https://www.fitaacademy.in/includes/assets/img/blog/software-testing.jpg" alt="testing" />
</p>
<h1 align="center">Software Testing🧪📊</h1>

Welcome! 👋 I'm currently taking a Software Testing🧪📊 course, and I've decided to share my notes right here 📓. I believe that taking notes helps us learn better, and I hope these notes can be valuable to others interested in Tesging(QA) engineering 🧪. Feel free to use this repository as a starting point 🚀, make edits to suit your needs 🖊️, and embark on an exciting journey into the world of QA 🌐. 

Happy coding ✨, and let's explore the realm of quality assurance together! 🌟

---

## Table of Contents 📬

- [1. Introduction to Software Testing 🦋](#introduction-to-software-testing-)
  - [What is Software Testing? 🚀](#what-is-software-testing-)
  - [Why is Software Testing Important? 🌐](#why-is-software-testing-important-)
- [2. The Software Testing Lifecycle (STLC) 🧪](#the-software-testing-lifecycle-stlc-)
- [3. Software Requirements: Requirements Analysis 🔍](#software-requirements-requirements-analysis-)
  - [User Story vs User Cases 📝](#user-story-vs-user-cases-)
  - [Requirements testing: 🧩](#requirements-testing-)
  - [What do we want from the analysis? 📊](#what-do-we-want-from-the-analysis-)
  - [Smart Requirements 🧠](#smart-requirements-)
  - [Use Flow Diagram 🌐](#use-flow-diagram-)
  - [Prototypes: 🤖](#prototypes-)
  - [Work Breakdown Structure (WBS): 🚀](#work-breakdown-structure-wbs-)
- [4. Test Types and Levels 📈](#test-types-and-levels-)
  - [Functional & Non-Functional Testing 💮](#functional--non-functional-testing-)
  - [Functional vs. Non-functional Testing: 🆚](#functional-vs-non-functional-testing-)
  - [Testing Types Based on System Access: 🧩](#testing-types-based-on-system-access-)
  - [Typical Test Objects: 💡](#typical-test-objects-)
- [5. Test Documentation 📝](#test-documentation-)
  - [Types of Test Documentation 📓](#types-of-test-documentation-)
- [6. Test Design Techniques 🧩](#test-design-techniques-)
  - [Black-box Test Design Techniques: ⚫️📊](#black-box-test-design-techniques-%EF%B8%8F)
    - [1. Equivalence Partitioning 🧪](#1-equivalence-partitioning-)
    - [2. Boundary Values 🛠️](#2-boundary-values-%EF%B8%8F)
    - [3. Pairwise Testing 🌐](#3-pairwise-testing-)
    - [4. Decision Table Testing 📓](#4-decision-table-testing-)
    - [5. State Transition Testing 🧩](#5-state-transition-testing-)
- [7. Defects and Bug Tracking 🐛](#defects-and-bug-tracking-)
  - [Mistake, Defect, and Failure in Software: 📈](#1-mistake-defect-and-failure-in-software-)
  - [Bug Report 📝](#2-bug-report-)
  - [Severity vs. Priority](#3-severity-vs-priority)
  - [Bug Life Cycle 🐛](#4-bug-life-cycle-)
  - [Bug Report Resolution: 📓](#5-bug-report-resolution-)
  - [Bug Tracking System: 📈🛡️](#6-bug-tracking-system-%EF%B8%8F)
- [8. Client Server Architecture API Testing 🦋](#client-server-architecture-api-testing-)
  - [Client 👻](#client-)
  - [Server 👾](#server-)
  - [Types of Client-Server Architecture 👽](#types-of-client-server-architecture-)
  - [Peer-to-peer 🤝](#peer-to-peer-)
  - [OSI models 👀](#osi-models-)
  - [Application Programming Interface (API) 🥷🏻](#application-programming-interface-api-)
- [9. Specifics of Different Applications Testing 👒](#specifics-of-different-application-testing-)
  - [Web Application Testing 💻](#web-application-testing-)
  - [Desktop Application Testing 🖥️](#desktop-application-testing-)
  - [Mobile Application Testing 📱](#mobile-application-testing-)
  - [Practical Tips for Testing Different Applications 🔮](#practical-tips-for-testing-different-applications-)
- [10. Test Metrics and Reporting 📜](#test-metrics-and-reporting-)
- [11. Software development methodologies 💫](#software-development-methodologies-)
- [12. Agile. Testing in Agile 💫](#agile-)
- [13. Test Planning 📑](#test-planning-)
- [14. Basics of Automation Testing. VCS, CI/CD. 💎](#basics-of-automation-testing-vcs-cicd-)


# Introduction to Software Testing 🦋
Software testing is a fundamental pillar of the software development process. It plays a pivotal role in ensuring that the software we use is reliable, efficient, and free from defects. In this repo, we'll embark on a journey to explore the fascinating world of software testing, starting with an introduction and a walkthrough of the Software Testing Lifecycle (STLC). So, let's dive in!

### What is Software Testing? 🚀
At its core, software testing is the process of evaluating a software application to identify and fix any issues or discrepancies. These issues could range from minor glitches to critical malfunctions that could affect user experience, security, or functionality. Software testing aims to ensure that the software performs as intended and meets user expectations.

### Why is Software Testing Important? 🌐
Imagine using a mobile app that crashes every time you open it or a website that doesn't load properly. Frustrating, right? This is where software testing becomes crucial. It helps detect and eliminate such problems, ensuring that the software works smoothly, performs efficiently, and offers a seamless experience to users. Moreover, testing also safeguards against potential security vulnerabilities.

# The Software Testing Lifecycle (STLC) 🧪
The Software Testing Lifecycle (STLC) is a systematic process that guides the testing of software applications. It comprises several well-defined phases, each with its unique purpose and activities. Let's take a closer look:

1. Requirement Analysis 📊 </br>
The first step in the STLC involves understanding the project requirements. Testing teams review these requirements to establish a comprehensive testing strategy. It's crucial to identify what needs to be tested, define testing objectives, and prepare a test plan.

2. Test Planning 💡 </br>
Once the requirements are clear, the test planning phase begins. Testers create a detailed test plan that outlines the testing scope, objectives, resources, and schedules. This plan acts as a roadmap for the entire testing process.

3. Test Design 🛠️ </br>
In this phase, test cases and test scripts are developed. These are step-by-step instructions that testers follow to conduct various tests. Test data and expected results are also prepared at this stage.

4. Test Environment Setup 📝 </br>
A suitable testing environment is essential for accurate testing. It replicates the real-world conditions in which the software will be used. This phase involves configuring the necessary hardware and software components for testing.

5. Test Execution 🧩 </br>
Now, it's time to put the test cases into action. Testers execute the tests as per the test plan, record the results, and compare them against expected outcomes. Any discrepancies are reported as defects.

6. Defect Reporting 🔍 </br>
When defects are identified during test execution, they are documented and reported to the development team. Clear and detailed bug reports help developers understand and resolve the issues efficiently.

7. Defect Re-Testing 🖊️ </br>
After the developers fix the reported defects, they are passed back to the testing team for re-testing. This ensures that the issues are resolved and the software is functioning correctly.

8. Regression Testing 📈 </br>
Changes made to the software can sometimes introduce new defects or impact existing functionality. Regression testing is carried out to ensure that no new issues arise as a result of these changes.

9. Test Closure 🎯 </br>
The final phase involves evaluating whether the testing goals have been met, and all test cases have been executed. A test summary report is prepared to document the testing process, its outcomes, and any remaining open issues.


# Software Requirements: Requirements Analysis 🔍
Requirements are a specification of what should be implemented. They are descriptions of how the system should behave, or of a system property or attribute

### User Story vs User Cases 📝
- User story is a simplified form of many users interacting with a software. 
- Use cases are very specific in relation to user stories.
- They describe specific user actions with any system.


### Requirements testing: 🧩
- Unaccounted for dependencies
- Testability
- Alternative flows in the business scenarios
- Check that there are no inconsistencies
- General logic about users’ feelings


### What do we want from the analysis? 📊
- Understanding business processes and the meaning of the user story
- Acceptance criteria
- Custom scripts
- Dependency analysis and impact on existing functionality

### Smart Requirements 🧠
Smart requirements are specific, measurable, achievable, relevant, and time-bound. They help ensure that project goals and objectives are well-defined and attainable. Here's a brief explanation of each component:

1. Specific: Requirements should be clear and precise, leaving no room for ambiguity. They should answer the who, what, when, where, and why of a project.
2. Measurable: Requirements should be quantifiable, allowing for objective assessment of success or completion. This often involves using metrics or criteria to evaluate progress.
3. Achievable: Requirements should be realistic and attainable within the constraints of the project, including time, resources, and budget.
4. Relevant: Requirements should directly contribute to the project's goals and objectives, ensuring that they are worthwhile and aligned with the project's purpose.
5. Time-bound: Requirements should have a defined timeframe or deadline, helping to manage project schedules and priorities effectively.

By adhering to SMART requirements, project managers and stakeholders can enhance project clarity, control, and success.


### Use Flow Diagram 🌐
A flow diagram is a visual representation of a process or system that uses symbols and arrows to illustrate the sequence of steps or components. It helps in understanding, analyzing, and communicating complex processes, making information more accessible and structured.

### Prototypes: 🤖
Prototypes are simplified, early versions of a product or system used to visualize, test, and refine its design and functionality. They help stakeholders better understand the final product and identify potential improvements or issues before full-scale development.

### Work Breakdown Structure (WBS): 🚀
A Work Breakdown Structure is a hierarchical diagram that breaks a project into smaller, manageable tasks or work packages. It provides a structured framework for organizing and planning project activities, making it easier to assign responsibilities, estimate resources, and track progress.


## Key Takeaways: 🔐
- Main two types of requirements: use cases and user stories
- The whole development team works with the requirements
- There are some requirements how the "ideal requirement" should look (SMART approach)
- Requirements testing approaches: User flow diagram, Prototypes and Work Breakdown Structure

# Test Types and Levels 📈

- Development Levels:
    
   💡 Development levels represent different stages in the creation of a product or system. These stages typically include design, coding, testing, and integration. Each level focuses on specific tasks and goals to gradually build and refine the final product.
    
- Test Levels:
    
  🧪 Test levels refer to distinct phases of the testing process during software development. They range from unit testing (testing individual components) to system testing (testing the entire system's functionality). Test levels ensure comprehensive evaluation of the product's quality and performance at various stages of development.

<img width="600" alt="Screenshot_2023-10-31_at_7 19 06_AM" src="https://github.com/mutasim77/QA-Notebook/assets/96326525/c837d5ca-a1c9-425e-85ca-489fe2412e3c">

A test type is a specific category of testing that focuses on checking different aspects of software quality, including:
1. ***Functional quality***, which looks at things like correctness and completeness. (e.g *What* does the system do? ) 🧪
2. ***Non-functional quality***, which assesses aspects like reliability, performance, security, compatibility, and usability. (e.g *How well* does the system work?) 📊
3. ***Structural or architectural correctness***, ensuring the software is built according to specifications. (e.g How the system works?) 🏗️
4. ***Testing the impact of changes***, which includes confirming fixes and checking for unintended consequences (regression testing). (Does the system work after a change?) 🔄


### Functional & Non-Functional Testing 💮

- ***Functional Testing:***
Functional testing assesses a system's functions, checking if it performs as expected. These functions are often described in documents like business requirements, user stories, or specifications. It evaluates "what" the system should do and can be done at various test levels. Black-box techniques are often used to create test cases, especially when testing software behavior. It may require domain-specific knowledge, like understanding the business problem the software solves. 🧪
- ***Non-Functional:***
Non-functional testing focuses on characteristics like usability, performance, and security. It evaluates "how well" the system behaves and is crucial at all test levels, preferably early in the process to catch defects before they become problematic. **Black-box** techniques are useful for creating test cases, such as using boundary value analysis for performance tests. You can measure the thoroughness of non-functional testing through non-functional coverage, ensuring you've addressed aspects like device compatibility for mobile applications. Late discovery of non-functional defects can be risky for a project's success. 📈🛡️🔍

### Functional vs. Non-functional Testing: 🆚

Functional testing checks what the software does, like its features and functions. Non-functional testing checks how it does it. Here are some key non-functional aspects:

- Reliability: Ensures the software works consistently and reliably. 🛡️
- Performance: Evaluates speed, responsiveness, and efficiency. 🚀
- Usability: Examines user-friendliness and ease of use. 👤
- Maintainability: Assesses how easy it is to maintain and update the software. 🛠️
- Security: Focuses on safeguarding against vulnerabilities and threats. 🛡️
- Compatibility: Checks if the software works well with different systems and browsers. 🌐
- Portability: Ensures the software can run on various platforms and devices. 📱💻


### Testing Types Based on System Access: 🧩

1. Black Box Testing: ⚫️📦  
    - Based on requirements and specified behavior.
    - Independent of the software's internal structure.
    - Test cases remain useful even if the implementation changes, as long as the required behavior stays the same.
    - Relies heavily on well-defined requirements.
    - Thoroughness measured by covering all stated requirements with test scenarios.
2. White Box Testing: ⚪️📦
    - Derives tests based on the system's internal structure, including code, architecture, workflows, and data flows.
    - Thoroughness measured through structural coverage, which assesses the extent of exercised structural elements.
    - Can focus on component code coverage or system architecture, depending on the testing level.
    - Involves knowledge of code, data storage, and the use of coverage tools.
3. Gray Box Testing: 🔘📦
    - Tester has partial knowledge of the system's internal structure, including access to documentation of data structures and algorithms.
    - Involves intelligent test scenario handling, like data types, communication protocols, and exceptions.
    - Requires both high-level and detailed documentation of the application.
    - Well-suited for web applications and functional/business domain testing.


### Typical Test Objects: 💡

1. Component Testing: 🛠️
    - Focuses on individual parts like components, units, or modules.
    - Involves testing code and data structures, classes, and database modules.
    - Typically conducted by the developer who wrote the code.
2. Integration Testing: 🐛
    - Tests the interaction of subsystems, databases, infrastructure, interfaces, APIs, and micro-services.
    - Ensures different components work together as a unified system.
3. System Testing: 🎯
    - Evaluates complete applications, hardware/software systems, operating systems, and the entire "system under test" (SUT).
    - Includes system configuration and configuration data.
4. Acceptance Testing: 💻
    - Validates the SUT in its entirety.
    - Assesses business processes for a fully integrated system.
    - Considers recovery systems and hot sites for business continuity and disaster recovery testing.
    - Examines operational and maintenance processes.

## Key Takeaways 🔐

1. Each test level is an instance of the test process, consisting of
activities performed in relation to software at a given level of
development, from individual units or components to complete
systems or, where applicable, systems of systems. Test levels
are related to other activities within the software development
lifecycle.
2. There are various test types and classifications depending on
the goal of the testing.
3. Every test type can be performed at any test level.
4. It is important to run applicable test types at each level,
especially at the earliest level where the test type occurs.


# Test Documentation 📝

- Test documentation includes various documents created before and during testing.
- It describes test coverage, execution, responsible parties, lists essentials, tracks issues, and more.
- Provides a central source for all testing information, ensuring clarity and organization.
- Helps turn informal processes into formal and structured ones.

### Types of Test Documentation 📓
<img width="600" alt="Screenshot_2023-10-31_at_7 57 30_AM" src="https://github.com/mutasim77/QA-Notebook/assets/96326525/1aee3efe-3bad-404d-8627-7e5bb94099e8">

- Test Policy: 🧪
    - A high-level document outlining testing principles, methods, and goals.
    - Collaboratively created by senior members of the test management team and stakeholder managers.
    - Goals include justifying the cost of quality, defining test objectives, measuring test efficiency, summarizing testing processes, and enhancing testing within the organization.
- Test Strategy: 🚀
    - A planning document detailing the scope, approach, resources, and schedule for testing activities.
    - Format and inclusion can vary among organizations, with some incorporating it within the test plan.
- Test Plan: 💡
    - High-level document identifying test levels, features to be tested, and key information.
    - Typically includes test schedule, priorities, regression test approach, roles, environment requirements, tools, risks, entry/exit criteria, and more.
    
- Test Scenarios: 🤖
    - Items or events in software that can be verified by one or more test cases.
    - Describes user-system interactions, including actors, preconditions, triggers, expected results, success scenarios, alternative paths, and post conditions.
    - Based on business requirements, system requirements, and assumptions.
    
- Test Cases: 🌐
    - A set of actions verifying specific application features based on test scenarios.
    - Include preconditions, test data, step-by-step instructions with expected results, priority, status, and additional information.
- Checklist: 📝 
    - Simplified test cases focusing on covering all possible user actions within a functionality.
    - Provide shorthand verifications, expected results, and status.
    - Useful for quick and efficient testing, but may lack detailed instructions for complex applications.
- Bug Report: 💻
    - Contains comprehensive information about a bug, including its description, severity, priority, and steps to reproduce.
    - Includes summary, version/build/environment, status, preconditions, actual and expected results, and attachments like logs and screenshots.
    - A well-documented bug report facilitates faster defect resolution.


## Key Takeaways 🔐
1. Test documentation is an important part of a QA’s daily activities as it helps to keep things in order. 
2. There are different levels of test documentation.
3. The main requirement of test documentation is to keep it simple and sufficient. Make sure it has all the necessary info and is not overloaded with unnecessary details.


# Test Design Techniques 🧩

### Test Design and Test Design Techniques:
- Test Design
    - The process of transforming general testing objectives into tangible test conditions and test cases.
- Test Design Technique
    - A procedure used to derive and/or select test cases.

### Test design goals: 🎯
- Provide optimal test coverage of the application:
    1. Tests should cover all functionality
    2. Tests should be minimal enough

### Test techniques are classified as:
- Black-box⚫️📦 → *Black-box testing analyzes requirements and system behavior without delving into its internal structure, making it suitable for both functional and non-functional testing.*
- White-box⚪️📦 → *White-box testing analyzes a system's internal structure, including its code, architecture, and design, in contrast to black-box testing, which looks at system behavior.*
- Experience-based🖊️ → *Experience-based test techniques use collective knowledge from developers, testers, and users to design and perform tests, often alongside black-box and white-box techniques.*

### Black-box Test Design Techniques: ⚫️📊

### 1. Equivalence Partitioning 🧪
- *Equivalence Partitioning* is a black-box testing method that creates test cases to represent different input or output groups, assuming the system behaves the same within each group, based on the specification. The goal is to cover each group at least once in the test cases (test at least one value from each class). It’s important to test valid and invalid equivalence classes.

- *Equivalence Partitioning* involves testing both **valid** and **invalid** values. Valid values should be accepted, forming valid equivalence partitions, while invalid values should be rejected, creating invalid equivalence partitions. Starting with valid data is a common practice in this method. It focuses on grouping similar data into equivalence classes, which include both valid and invalid values.

#### Algorithm for using the technique: 🧠
1. Define equivalence classes.
2. Pick a representative from each class.
3. Perform tests for each equivalence class.

### 2. Boundary Values 🛠️
- ***Boundary Value Analysis*** is a black-box testing technique that focuses on testing values at the boundaries of equivalence partitions. Boundary values are the values right at the edge of these partitions. 

- The algorithm involves defining the range of values (an equivalence class), identifying the boundary values, creating three test cases for each boundary, and executing the tests for these boundary values. The goal is to test the system's behavior at the edges, where issues often arise.

### 3. Pairwise Testing 🌐
- ***Pairwise Testing*** is a black-box testing technique designed to efficiently test all possible combinations of input parameters in pairs. Instead of testing all possible combinations for all values of the variables, it focuses on testing all pairs of variables. This method significantly reduces the number of test cases needed while still ensuring comprehensive coverage. It's especially useful when dealing with a large number of possible combinations.

### 4. Decision Table Testing 📓
- Decision Table Testing*** is a *black-box* testing technique where test cases are designed to execute combinations of inputs and stimuli specified in a decision table. This method is useful for recording complex business rules, ensuring that all possible condition combinations have been considered, and easily identifying missed conditions.
    - **Conditions:** Represent input conditions and can be Boolean or have multiple values.
    - **Actions:** Define processes to be executed based on input parameter combinations.
    - **Rules:** Describe unique combinations of conditions leading to specific actions.
Decision table testing aims to achieve 100% coverage of all condition combinations, helping find gaps or requirements' lack of clarity.

### 5. State Transition Testing 🧩
- ***State Transition Testing*** is a black-box testing technique that employs a state transition diagram or state table to create test cases. These test cases evaluate if a system successfully executes valid transitions while preventing invalid transitions.

- **State Transition:** It represents a change from one state to another in a component or system.

- State transition testing is useful when a system has states and needs to respond to real-time events from outside the system. It's not applicable when the system lacks states or doesn't require responses to external real-time events.

### Key Takeaways 🔐

1. The test design's goals are to provide optimal test coverage of the application.
2. Test techniques are classified as *Black-box, White-box, and Experience-based.*
3. Main Black-box test design techniques:
    - 1. *Equivalence partitioning* — test cases are designed to execute representatives from equivalence partitions.
    - 2. *Boundary value analysis* — test cases are designed based on boundary values of equivalence partitions.
    - 3. *Pairwise testing* — test cases are designed to execute all possible discrete combinations of each pair of input parameters.
    - 4. *Decision Table Testing*: Test cases are created to execute combinations of inputs and stimuli as specified in a decision table.
    - 5. *State Transition Testing:* Test cases are based on state transition diagrams or state tables and typically involve sequences of events leading to state changes (and possible actions). A single test case can cover multiple state transitions. These techniques focus on testing different aspects of a system's behavior without delving into its internal structure.

# Defects and Bug Tracking 🐛

### 1. Mistake, Defect, and Failure in Software: 📈
- **Mistake:** A human error or oversight in the software development process.
- **Defect (Bug):** An error, flaw, or fault in the software that causes it to produce an incorrect or unexpected result, or behave in unintended ways. It's an inconsistency between actual and expected behavior.
- **Failure:** The software's inability to meet its intended functionality, often caused by defects.

***The First Computer "Bug":*** 🐛💻
     On September 9, 1947, Grace Hopper encountered the first computer bug. It was a physical moth stuck between a relay in the Harvard Mark II computer, causing a malfunction. Hopper recorded this incident as the "First actual case of a bug being found." This term, "bug," has since become synonymous with software defects.

---

### 2. Bug Report 📝
A bug report is a document that highlights any flaw in a component or system that can disrupt its intended functionality. The purposes of creating a bug report are:

1. **Notification:** It informs the development team and other relevant individuals with a detailed description of the problem.
2. **Prioritizing:** It helps define the potential impact on the project and the desired time for elimination.
3. **Assistance for the Fix:** A well-structured bug report, which includes an analysis of the problem and possible root causes, can serve as the first step in resolving the bug.

***General Tips for Bug Reports:***
- Report all identified bugs.
- Write the report clearly and politely.
- Focus on one problem per issue for easier processing.
- Provide objective facts about the bug rather than speculative explanations.
- Reproduce the bug before reporting to ensure clarity.
- Test for the same defect in similar modules, as developers often reuse code across multiple areas, increasing the likelihood of the issue occurring in other parts.

***Bug Report Attributes:*** 🤖
- **Defect ID:** A unique identification number for the bug.
- **Summary:** A concise description of the bug.
- **Project:** The name of the project the bug relates to.
- **Affected Version:** The version in which the bug was discovered.
- **Fix Version:** The version in which the bug is expected to be resolved.
- **Reported By:** The individual who reported the bug.
- **Assigned To:** The person responsible for fixing the bug.
- **Status:** Indicates the current status of the defect (e.g., Open, In Progress, Testing, Closed, Reopened, etc.).
- **Severity:** Reflects the impact of the defect on the application.
- **Priority:** Indicates how urgently the bug needs to be addressed.
- **Steps to reproduce (STR)** — steps that need to be performed to reproduce the bug
- **Actual result** — what happens after the STR are executed
- **Expected result** — what should happen after the STR are executed
- **Preconditions** - Special conditions that need to be performed before attempting to reproduce the bug
- **Attachments** - Screenshots, videos, logs, and files which will help to understand the root cause

***Tips for Writing Bug Descriptions:*** 📝
1. **Clarity is Key:** Ensure your bug report is clear and concise, allowing others to consistently reproduce the issue.
2. **Reproduce the Bug:** Find the precise steps to consistently reproduce the bug.
3. **Be Specific:** Avoid vague phrases like "I clicked on the link." Instead, use specific actions like "Click the 'Login' link."
4. **Include Preconditions:** If necessary, add any prerequisites or conditions that are relevant to reproducing the bug.
5. **Test Your Own Instructions:** Pretend you are someone else following your instructions to validate their clarity.
6. **Actual vs. Expected:** After providing steps, detail what actually happened (actual result) and what you expected to happen (expected result).
7. **Provide System Details:** Specify the operating system, web browser, device, or any other relevant environmental information. This aids in isolating the problem and fixing it.


***Tips to Create Attachments:*** 💻
1. **Screenshots** →  *Highlight the area that contains the bug. If you need to show a multiple places you can use enumeration.*
2. **Text Files** → *Attachments should aid developers in issue resolution, including log files, input/output data in standard formats, and error messages, while avoiding proprietary file types like .docx and ensuring they contain relevant bug-related information.*
3. **Video** → *Video evidence should align with the reported steps, be trimmed to show only the bug, and be provided when steps are complex, with attention to file size limitations in bug-tracking systems.*

### 3. Severity vs. Priority
So, to put it simply, severity is about how bad a problem is, and priority is about how quickly we need to fix it. We use these two things to decide which problems to fix first when we're testing and making things better.

***Severity Degree of Impact:*** 🛡️
1. Blocker 
2. Critical
3. Major
4. Minor
5. Trivial
   
***Priority Degree of urgency:*** 🛡️
1. High
2. Medium
3. Low

### 4. Bug Life Cycle 🐛
<img width="600" alt="Screenshot_2023-10-31_at_11 01 28_AM" src="https://github.com/mutasim77/QA-Notebook/assets/96326525/9546ac93-18fd-4600-b36a-242e83c28ef4">

### 5. Bug Report Resolution: 📓
The Resolution field is employed to indicate how issues are resolved. Potential resolutions encompass:
- **Fixed:** The bug was rectified by modifying the source code.
- **Won't Fix:** A decision was made not to address the bug.
- **Can't Reproduce:** The bug cannot be replicated.
- **By Design:** The person reporting the bug had a misconception about the software's intended operation, and it is functioning correctly.
- **External:** The bug results from an external factor unrelated to the software.
- **Duplicate:** The bug has already been reported.

### 6. Bug Tracking System: 📈🛡️
A system for receiving and filing bugs reported in a software project and tracking those bugs until they are fixed. (e.g JIRA, Mantins)

## Key Takeaways 🔐
1. A bug report is a detailed instruction how to reproduce a bug
2. A bug report should always list the expected and actual results
3. A bug report is an instruction on how to reproduce a bug
4. A bug always has expected and actual results
5. Severity is the degree of impact to the system
6.  Priority is the level of importance
7. The main workflow for bugs is: New, Assigned, Resolved, Closed
8.  Bug Tracking Systems all provide the same basic functionality


# Client Server Architecture API Testing 🦋

Client-server architecture is a computing model where a central server hosts and delivers resources to clients. This gives the server complete control over the network and its devices. Users can access any file on the central storage, and resources can be easily shared across different platforms.

Here is a breakdown of the bullet points:

- The server has complete control over the network and its devices.
- All devices in the network can be controlled centrally.
- Users can access any file on the central storage at any time.
- Resources can be easily shared across different platforms.

### Client 👻
A **user** is a person who interacts with a software application,
system, or device to achieve a certain goal or task. The user is
the individual for whom the technology is designed and who
uses it to perform actions, access information, or utilize services

### Server 👾
A server is a specialized computer hardware system or software
application designed to provide services, resources, or data to
other computers, devices, or clients over a network

- **Service Provider**: A server provides services to other devices over a network. For example, a web server provides the web pages that you view when you visit a website.
- **Centralized Processing**: A server can be used to centralize the processing of data and applications. This can improve performance and efficiency.
- **Always On**: Servers are typically designed to be always on, so that they are always available to provide services to clients.
- **Communication Hub**: A server can act as a communication hub for devices on a network. For example, a mail server can be used to send and receive emails between -devices on a network.
- **Data Storage**: A server can be used to store data for other devices on a network. This can make it easier to access and share data.
- **Security and Access Control**: A server can be used to implement security measures and control access to data and resources.
- **Scalability**: Servers can be scaled up or down to meet the needs of a growing or shrinking network.

### Types of Client-Server Architecture 👽
1. 1-Tier (Single Computer, Monolith) - This kind of architecture contains all sorts of settings on a single device
2. 2-Tier Client Server Architecture, the whole application logic is divided into 2 parts. The database logic and business logic need to be maintained, where this logic is stored either on the client’s end or the server’s end. When the logic is stored on the client’s end, the architecture is called “fat client, thin server” However, if the logic is handled by the server then we call it “thin client, fat server”.
3. 3-Tier architecture all three layers, the presentation layer, the application layer, and the database, layer are placed at different points.

### Peer-to-Peer 🤝
Peer-to-peer (P2P) is a network where computers share files and resources directly with each other, without the need for a central server. This is in contrast to the traditional client-server model, where computers communicate with a central server to access files and resources.

### OSI model 👀
The 7 layers of the OSI model are a conceptual framework for understanding how networks work. Each layer performs a specific function, and the layers work together to provide reliable and efficient communication between devices.

- Layer 7: Application
This layer provides services to end-user applications, such as web browsers, email clients, and file transfer programs.
- Layer 6: Presentation
This layer formats data for the application layer and handles encryption and decryption.
- Layer 5: Session
This layer manages the communication session between two devices, such as setting up and tearing down the connection.
- Layer 4: Transport
This layer ensures reliable end-to-end communication between two devices. It also provides services such as flow control and congestion control.
- Layer 3: Network
This layer routes data packets between different networks. It also provides services such as IP addressing and subnetting.
- Layer 2: Data Link
This layer controls how data is transmitted over a physical link. It also provides services such as error detection and correction.
- Layer 1: Physical
This layer is responsible for the physical transmission of data over a medium, such as a cable or radio waves.

### Application Programming Interface (API) 🥷🏻
**SOAP vs. REST**
• SOAP is a protocol whereas REST is an architectural pattern.
• SOAP uses service interfaces to expose its functionality to client
applications while REST uses Uniform Service locators to
access the components on the hardware device.
• Comparing SOAP vs REST APIs, SOAP only works with XML
formats whereas REST work with plain text, XML, HTML, and
JSON.
• SOAP cannot make use of REST whereas REST can make use
of SOAP.

## Key Takeaways 🔐
1. Client server architecture is a part of a networking model that
allows multi-user updates through a graphical user interface to
a shared database
2. API testing has the ability to improve test coverage and
efficiency, secure the system, and much more
 - Earlier Validation
 - Easier Test Maintenance
 - Faster Time to Resolution
 - Speed and Coverage


# Specifics of Different Applications Testing 👒

## Web Application Testing 💻
A **web application** is software that utilizes web browsers and web technologies to perform tasks over the Internet.
A web application has a client-server architecture, so test process should take into account all three parts to verify - the client, the server and communication (API).


### Functional Testing:
- Completeness: All specified tasks and user objectives are covered.
- Correctness: Results are accurate and precise.

**Client Side:**
- Navigation, Forms, Data Display and Interaction, Validation Messages, etc.
- Localization and Internationalization

**Server Side:**
- Test the server's API endpoints by sending requests and validating the responses;
- Ensure that the server interacts correctly with the database by testing data retrieval, insertion, updating, and deletion operations.

### Performance Testing 🚀
This characteristic represents the performance relative to the amount of resources used under stated conditions:
- Time behavior – the response and processing times of a product when performing its functions.
-Resource utilization – the amount and type of resources used by a product, when performing its functions

**Client Side:**
- Load Time and Page Speed Testing.
- Resource Optimization - excessive resource usage (e.g., memory, CPU) on the client side.
- Caching

**Server Side:**
- Load Testing - how well the server performs under heavy loads by simulating a large number of concurrent users or requests.
- Performance Testing - measuring response times and resource utilization. Identify and address bottlenecks.

### Compatibility Testing 🔄
A compatibility test is an assessment used to ensure a software application is properly working across different browsers, databases, operating systems (OS), mobile devices, networks and hardware.

**Client Side:**
- Browser Compatibility - test the application on different web browsers (e.g., Chrome, Firefox, Safari, Edge).
- Cross-Device and Cross-Platform Testing:
  - Mobile - application is functional and responsive on various mobile devices and screen sizes.
  - Cross-Platform: Test the application on different operating systems (e.g., Windows, macOS, iOS, Android).
 
**Server Side:**
- Test the server-side application on different environments, platforms, and configurations to ensure it works correctly across various setups.

### Usability Testing 👌
The degree to which a product or system can be used by specified users to achieve specified goals with effectiveness, efficiency, and satisfaction within a specified context of use:
- Appropriateness recognizability
- Operability
- User error protection
- User interface aesthetics
- Accessibility

**Client Side:**
- User Experience (UX) Testing:
   - Usability Testing - user-friendliness of the application.
   - Accessibility Testing - ensure the application is accessible to users with disabilities

### Reliability Testing ⚙️
Degree to which a system or component performs specified functions under specified conditions for a specified period of time:
- Availability – the system is operational and accessible.
- Fault tolerance – the system operates as intended despite the presence of hardware or software faults.
- Recoverability

**Client Side:**
- Offline Functionality Testing - Test how the application behaves when the user is offline or in low-network conditions if it includes offline capabilities

**Server Side:**
- Availability – business logic (endpoints) are available upon client requests
- Failover and Recovery – the ability to recover gracefully from failures, including hardware failures, network issues, and software crashes.

### Security Testing 🔒
Degree to which system protects information and data so that persons or other products or systems have the degree of data access appropriate to their types and levels of authorization:
- Confidentiality
- Integrity
- Authenticity

**Client Side:**
- Authentication and Authorization
- Client-Side Security - common client-side security vulnerabilities such as Cross-Site Scripting and Cross-Site Request Forgery

**Server Side:**
- Test the server for vulnerabilities and security issues, including SQL injection, cross-site scripting (XSS), and other common security threats.
- Authentication

### Maintainability Testing 🛠️
This characteristic represents the degree of effectiveness and efficiency with which a product or system can be modified to improve it, correct it or adapt it to changes in environment, and in requirements:
- Modularity
- Analyzability
- Modifiability
- Testability

**Client and Server Side:**
- Clean and Readable Code
- Modularity - breaking down a software system into smaller, modular components or functions makes it easier to work on individual pieces without affecting the entire system.
- Error Handling and Logging - Proper error handling and logging mechanisms.
- Scalability - Designing the system with scalability in mind allows for easier adaptation to increased load

### Portability Testing 🌐
Degree of effectiveness and efficiency with which system can be transferred from one hardware, software, or other operational or usage environment to another:
- Adaptability - system can effectively be adapted to different or evolving hardware
- Installability
- Replaceability

**Server Side:**
- Install - software can be installed successfully without any critical errors or failures.
- Upgrade - ability to upgrade from a previous version.
- Clean Uninstallation - software can be uninstalledcleanly, removing all installed files, registry entries, and associated components.
- Recovery Point - system can be restored to its previous state after uninstalling the software

### Key Takeaways 🔐
- Quality is a combination of various characteristics
- Despite the various test types carried out, the context of web testing can be different depending on the specifics of the application (e.g., the testing of a bank application can be different from that of an online shop)
- Frontend and backend validation

## Desktop Application Testing 🖥

Works on a desktop Operation System
- Requires installation
- Better use of computer resources, better performance
- Can use various components and devices connected to a Personal Computer (laptop), like a webcam, microphone, printer, etc.
- Can vary in complexity – from calculator and notepad to engineering calculation and video rendering

### Functional Testing
Desktop applications usually differ in terms of complexity and functionality.
- Test individual features and functions of the application to ensure they work as intended.
- Verify that the application performs calculations, processes data, and executes tasks accurately.

### Performance Testing
- Resource Utilization: Desktop applications have access to the full resources of the user's computer, including CPU, memory, and storage. They can efficiently utilize these resources to deliver high-performance experiences.
- Local Execution: Desktop applications run directly on the user's machine, eliminating the need to transmit data and instructions over the internet.
- Direct Access to Hardware: Desktop applications can directly interact with hardware peripherals and devices connected to the user's computer, such as printers, cameras, and sensors.

### Compatibility Testing 🔄
- Identify Target Environments: Determine the target platforms, including different versions of operating systems (e.g., Windows 7, Windows 10, macOS) and hardware configurations (e.g., 32-bit vs. 64-bit, different CPU architectures).
- Device testing: Device testing makes certain that the app functions consistently with each applicable device, such as Bluetooth devices, scanners, printers, etc.

### Usability Testing 👌
Perform usability testing to evaluate how easily users can navigate the application, learn its features, and perform tasks. Assess the application's user interface for attractiveness.
- Understandability
- Learnability
- Operability
- Attractiveness

### Reliability Testing ⚙️
The primary goal is to ensure that the desktop application functions consistently without crashes, errors, or unexpected failures, even under prolonged use and varying conditions.
- Stress and Load Testing
- Performance Monitoring
- Long-Running Tests

### Security Testing 🔒
- Access to Application - Some programs only need the basic permissions allowed by the OS, others require granting the user more control through administrative privileges.
- Authentication and Authorization
- Data Protection (Data Encryption) - data is properly encrypted during storage and transmission.
- Input Validation and Sanitization

### Maintainability Testing 🛠️
- Modularity – the degree to which a system or computer program is composed of discrete components, so that a change to one component has minimal impact on other components.
- Reusability – the degree to which an asset can be used in more than one system, or in building other assets.
- Modifiability – the degree to which a product or system can be effectively and efficiently modified without introducing faults or degrading existing product quality.

### Portability Testing 🌐
- Install - software can be installed successfully without any critical errors or failures.
- Upgrade – the ability to upgrade from a previous version.
- Clean Uninstallation - software can be uninstalled cleanly, removing all installed files, registry entries, and associated components.
- Recovery Point – the system can be restored to its previous state after uninstalling the software.

### Key Takeaways
- Desktop applications run on various operating systems (e.g., Windows, macOS, Linux) and may have different versions for each.
- Installation and Configuration: Verification of the installation process, ensuring that the application can be installed, updated, and uninstalled without issues.
- Offline Functionality: Unlike web applications, desktop apps can operate offline.
- Resource Utilization: Desktop applications have access to the local machine's resources (CPU, memory, storage). 

## Mobile Application Testing 📱
- A mobile application, often referred to as a "mobile app", is a software program designed specifically to run on mobile devices, such as smartphones and tablets.
- They are generally small, individual software units with limited
function:
  - Gaming
  - Social Media
  - Utility
  - E-commerce
  - Communication
 
### Functional Testing
- Application operation when running/exiting meets the basic requirements.
- Ensure the application goes into the background in the case of an incoming call.
- Check if the phone can store, receive, and send messages while the application is running.
- Make sure the device works in multitasking mode when necessary.
- Ensure the installed application does not prevent the normal operation of other applications and does not consume their memory

### Performance Testing 🚀
- To determine whether the application performs as per the requirement under different load conditions
- To validate CPU utilization
- To determine whether the current network coverage is able to support the application during peak, average, and minimum load levels
- To evaluate whether the battery life can support the application to perform under projected loads

### Compatibility Testing 🔄
- Device Compatibility: Mobile devices come in various sizes, resolutions, and hardware configurations.
- Operating System Compatibility: Mobile apps need to be tested on different versions of the operating systems they support (e.g., iOS, Android).
- Browser Compatibility: For mobile web apps, compatibility testing involves checking how the app performs on various mobile web browsers like Safari, Chrome, Firefox, and Edge.
- Third-Party Integrations: Compatibility testing verifies that any third-party libraries, APIs, or services used by the app work seamlessly across various environments.

### Usability Testing 👌
- Assess User Experience: Determine how users interact with the app, their overall satisfaction, and their ability to achieve their goals while using it
- Identify Usability Issues: Discover any usability problems, such as confusing navigation, unclear instructions, or frustrating interactions, that may hinder the user experience
- Gather User Feedback: Collect valuable feedback from real users about what works well in the app and what needs improvement
- Improve Design and Functionality: Use the insights gained from usability testing to make the necessary design and functionality enhancements to the app

### Reliability Testing ⚙️
Reliability testing aims to ensure that the software operates as intended consistently, with no unexpected failures or disruptions.
- Stress and Load Testing
- Performance Monitoring
- Long-Running Tests

### Security Testing 🔒
- Detection of Vulnerabilities: Timely detection of vulnerabilities ensure that flawed application susceptible to malicious attacks isn’t released by the developers.
- Elimination of Vulnerabilities
- Maintain Compliance: Mobile applications are strictly required to maintain compliance since many such applications deal with payments and customer personal information.
- Free of Security Risks: Mobile application security testing successfully secures one’s application against any risks that could result in data breaches, theft, or loss of confidential information.

### Maintainability Testing 🛠️
- Modularity – the degree to which a system or computer program is composed of discrete components, so that a change to one component has a minimal impact on other components.
- Reusability – the degree to which an asset can be used in more than one system, or in building other assets.
- Modifiability – the degree to which a product or system can be effectively and efficiently modified without introducing faults or degrading existing product quality

### Portability Testing 🌐
- Install - software can be installed successfully without any critical errors or failures.
- Upgrade - ability to upgrade from a previous version.
- Clean Uninstallation - software can be uninstalled cleanly, removing all installed files, registry entries, and associated components.
- Application Markets Policies

### Key Takeaways 🔐
- There are different types of mobile applications (web, native, hybrid) that require diversity in the specifics of testing
- The most common issues found in mobile applications are loading problems or a deficient or lacking in performance, unresponsive elements, displaying on various resolutions, etc

# Practical Tips for Testing Different Applications 🔮

## Web Application 💻 

### Web Application Testing – Functionality and UI

UI testing is used to verify if the functional attributes comprising the product's design work according to the user’s expectations, to check the product's simplicity, and that they work as expected.
- Test forms are working as expected.
- Test HTML and CSS to ensure that search engines can crawl your site easily.
- Test that all links on your web pages are working correctly and ensure there are no broken links.

### Web Application Testing – Web API
In API Testing, instead of using standard user input (keyboard) and output, you use software to send calls to the API, obtain the output, and note the system’s response. API tests are very different from GUI Tests and don’t pay attention to the look and feel of an application. It is mainly concentrated on the business logic layer of the software’s architecture.

### Web Application Testing – Internet Connection
Network Throttling is an intentional method to slow down the speed of the internet connection. It is used to analyze web performance where network throttling or network condition emulation is used to emulate low bandwidth conditions.

### Web Application Testing – Security
The OWASP Top 10 is a standard awareness document for developers and web application security. It represents a broad consensus about the most critical security risks to web applications.
Security testing of any system is focused on finding all possible loopholes and weaknesses of the system, which might result in a loss of info. It focuses on finding all potential loopholes and weaknesses of the system which might result in the organization’s loss of information or loss of reputation for the organization.

### Web Application Testing – Performance
Features and Functionality supported by a software system are not the only concern. A software application’s performance, like its response time, reliability, resource usage, and scalability, do matter. The goal of Performance Testing is not to find bugs but to eliminate performance bottlenecks.
- Load testing
- Stress testing
- Endurance testing
- Volume testing

### Web Application Testing – Cross-browsing
Browser vendors follow Open Web Standards, but they have their own interpretations of it. Since they each render HTML, CSS, and JavaScript in unique ways, thoroughly debugging your website’s source code is not enough to ensure that your website will look and behave as intended on different browsers (or different versions of a single browser). Cross browser testing helps with that by pinpointing browser-specific compatibility errors.

## Desktop Application 🖥️

### Desktop Application Testing - Installation

- Ensure that the installation process is well-documented.
- Verify the proper installation of dependencies such as libraries, drivers, and components.
- Ensure that the installation works properly on the required operating system and hardware configurations.
- Test the installation on multiple environments, as different hardware and software configurations may cause variations in the process.
- Check that the program runs after installation

### Desktop Application Testing - Performance

- Measure response times and resource utilization (CPU, memory, disk, network) under load.
- Evaluate how the application performs under expected user loads.
- Monitor for memory leaks, crashes, and resource exhaustion

## Mobile Application 📱

### Mobile Native Application Testing
Mobile native apps need to be tested across various mobile devices and operating systems to check their compatibility, usability, and consistency.
- For a native app, installation is required but for mobile web apps, no installation is required.
- Native apps are installed and updated from app stores like Google Play Store or App Store while mobile web apps have centralized updates.
- Store policies that are designed to deliver apps and games safely to billions of people worldwide
  - <a href="https://play.google.com/about/developer-content-policy">Play Google Content Policy</a>
  - <a href="https://developer.apple.com/app-store/review/guidelines">App Store Guidelines</a>

- A mobile device is a system that does not have powerful components, so it can’t operate like a personal computer.
- Native apps have single-platform affinity while mobile web apps have cross-platform affinity.
- Native apps work faster when compared to mobile web apps.
- Check screen orientation in landscape and portrait mode.
- Native apps built-in device features like camera, location access, push notifications.
- Connectivity testing with various bandwidths or offline mode.
- Interruption testing – incoming calls, messages, notifications.
- Device resources usage – CPU, memory, battery
- How the application works in energy saving mode
- How the application behaves when stored in the background

### Key Takeaways 🔐
- Different applications have their own specifics of operation and testing
- Functional testing counts to be the main and high priority verification
- A variety of tools exist that can help QA engineers with their test activities

# Test Metrics and Reporting 💫

### Test Monitoring and Controlling: Monitoring
Monitoring is a process of collecting, recording, and reporting information about the project's activities that the project manager and stakeholder need to know.

In order to monitor the process the Test Manager performs the following activities:
- Defines the project's goals or project's performance standards.
- Observes the project's performance and compare this to the actual and the planned performance expectations.
- Records and reports any detected problems which happen with the project.

Controlling is the process of using data from the monitoring activities to bring actual performance up to the level of the planned performance. In this step, the Test Manager takes actions to correct the deviations from the plan. In some cases, the plan has to be adjusted according to the situation with the project.

### Cost-Schedule-Resources-Quality
Monitoring will allow you to make comparisons between your original plan and your progress so far. You will be able to implement changes, where necessary, to complete the project successfully. You should monitor the key parameters as below:
- Cost
- Schedules
- Resources
- Quality

### Costs
- Costs are an important aspect of project monitoring and control.
- You have to estimate and track the basic cost information for your project.
- Having accurate project estimates and a robust project budget is necessary to deliver the project within the determined budget.

### Schedule
The schedule tells you:
1. When should each activity be done?
2. What has already been completed?
3. The sequence in which things need to be finished.

### Resources
- Resources are everything that is required to carry out the project's tasks.
- They can be the people or equipment that are required to complete the project.
- A lack of resources can affect the project's progress.

### Quality
Quality monitoring involves monitoring the results of specific products of the work (like test case suite, test execution log), to evaluate whether they meet the defined quality standards. In case the results do not meet the quality standards, you need to identify potential solutions.

### Why Did You Miss the Deadline?
- I forgot to monitor and control the project's progress.
- My team members did not work well.
- Developers finished their work too late.
- The test team was very slow with testing.
- I don’t know why

### Test Control
Test control is basically about controlling and taking corrective measures based on the results of test monitoring.

Examples include:
- Prioritizing the testing efforts
- Revisiting the test schedules and dates
- Reorganizing the test environment
- Reprioritizing the test cases/conditions

## Testing Metrics 👀

### What are Software Testing Metrics?

In software testing, a metric is a quantitative measure of the degree to which a system, system component, or process possesses a given attribute. In other words, metrics help to estimate the progress, quality, and health of software testing efforts.
- A good example of metrics would be the weekly mileage of a car compared to its ideal mileage recommended by the manufacturer.

### Why Do We Need Test Metrics?
- Take decisions for the next phase of activities.
- Evidence of claims or predictions.
- Understand the types of improvements required.
- Take decisions or make process or technology changes.

### Metrics Lifecycle
1. Analysis:
   - Identify the Metric(s) to use.
   - Define the Metric(s) identified.
   - Define the parameter(s) for evaluating the metric(s) identified.
2. Communiqué:
   - Explain the need for the metric to stakeholders and the testing team.
   - Educate the testing team about the data points that need to be captured for processing the metric.
3. Evaluating:
   - Capture the data.
   - Verify the data.
   - Calculating the metric(s) value using the data captured.
4. Reporting:
   - Develop the report with an effective conclusion.
   - Distribute the report to stakeholders and their representatives.
   - Take feedback from stakeholders.

### Types of Metrics
1. Process Metrics:
   - Can be used to improve the process efficiency of the Software Development Life Cycle.
2. Product Metrics:
   - Deal with the quality of the software product.
3. Project Metrics:
   - Can be used to measure the efficiency of a project team or any tools being used by the team members.

### How to Calculate Test Metrics?
To understand how to calculate software test metrics, we can look at an example of percentage test cases executed. 
To obtain the execution status of the test cases as a percentage, we use the formula.
**Percentage of test cases executed = (Number of test cases executed / Total number of test cases written) x 100**
Likewise, you can calculate other parameters like _test cases not executed_, _test cases passed_, _test cases failed_, _test cases blocked_, etc.


### What are Test Summary Reports?
A test summary report is a document which contains:
- A summary of test activities and final test results.
- An assessment of how well the testing was performed.
Based on the report, the stakeholders can:
- Evaluate the quality of the tested product.
- Decide whether to release the software.

For example, if the test report shows that there’re many defects remaining in the product, the stakeholder can delay the release until all the defects are fixed.

## Key Takeaways
- Monitoring and Controlling — two processes that Test Manager should do.
- Software Testing Metrics are essential indicators of the efficiency and effectiveness of software testing processes.
- Don’t forget about visualization.
- Test Summary Report — one of the critical instruments to show customers what we are doing.


# Software development methodologies 💫

## Software Development Life Cycle(SDLC) 📑
A software development lifecycle model defines how different development phases and types of activities performed within this process relate to each other, both logically and chronologically
- Each phase of a SDLC is followed by a formal review which helps to optimally control the management of it
- It ensures that all the stakeholders are aware of the project’s state and its planning
- Provides a plan for management and lowers project risk
- Delivers high-quality software applications in line with the client’s expectations

## Testing in SDLC 👒
In any software development lifecycle model, there are several characteristics of good testing:
- For every development activity, there is a corresponding test activity
- Each test level has test objectives specific to that level
- Testers participate in discussions to define and refine requirements and design, and are involved in reviewing work products (e.g., requirements, design, user stories, etc.) as soon as drafts are available
- No matter which software development lifecycle model is chosen, test activities should start in the early stages of the lifecycle, adhering to the testing principle of early testing.

## Sequential Models ✨
**What it means**: Following a step-by-step approach in software development, where each phase is completed before moving to the next.
**Example**: Waterfall model - Planning, then coding, testing, and so on.

### Waterfall Model 🥷🏻
A sequential development model that describes the software development process as a linear, sequential flow of activities. This means that any phase in the development process should begin when the previous phase is complete. 
In the Waterfall model, the development activities (e.g., requirements analysis, design, coding, testing) are completed one after another. In this model, test activities only occur after all other development activities have been completed. 

### V-model 💎
Unlike the Waterfall model, the V-model integrates test processes throughout the development process, implementing the principle of early testing. Furthermore, the V-model includes test levels associated with each corresponding development phase, which further supports early testing. In this model, the execution of tests associated with each test level proceeds sequentially, but in some cases overlapping occurs.

## Iterative and Incremental 🦋
**What it means**: Developing software in smaller parts, improving and adding features in cycles.
**Example**: Agile development - Releasing a basic version, then enhancing and adding features in regular iterations.

## Lean 🪄
**What it means**: Focusing on efficiency, minimizing waste, and delivering value without unnecessary steps.
**Example**: Lean software development - Streamlining processes, eliminating non-essential tasks to deliver a streamlined product.

## Key Takeaways 🔐 
- The software development life cycle is an important process for any software development project. It helps create high-quality products, manage time and resources, and track progress more accurately.
- There are different SDLC models: sequential, iterative, incremental, lean, etc.
- It must be selected and adapted to the context of the project and product characteristics - project goal, the type of product being developed, business priorities, project risks, etc.

# Test Planning 📑
## Contextual Factors That Influence the Testing Process
- The software development life cycle model and project methodologies being used
- Test levels and test types being considered
- Business domain
- Product and project risks
- Operational constraints, including but not limited to budgets and resources, timescales, complexity, contractual and regulatory requirements
- Organizational policies and practices
- Required internal and external standards

## Testing Process and Activities
- Test planning
- Test monitoring and control
- Test analysis
- Test design
- Test implementation
- Test execution
- Test completion

### Contextual Factors:
- Definition: These are the conditions and situations that can influence your testing approach.
- Example: If you're testing a mobile app, the contextual factors could include different devices (phones and tablets) and operating systems (iOS and Android).

### Testing Process:
- Definition: The step-by-step activities and tasks you follow to ensure a product works as intended.
- Example: In testing a website, the process may involve checking links, forms, and page navigation. If any link doesn't work or a form doesn't submit properly, that's a part of the testing process to identify and fix those issues.

### Risks in Testing:
- Definition: Potential problems or challenges that may affect the success of your testing efforts.
- Example: A risk in testing an e-commerce platform could be insufficient security measures, leading to the possibility of unauthorized access to customer data. Identifying and addressing this risk is crucial to ensure the safety of user information.

### Test Plan:
- Definition: A document outlining what you're going to test, how you'll test it, and the resources needed.
- Example: For testing a new software release, a test plan might include details like which features to test, the testing schedule, the team members responsible for each task, and the testing tools to be used.


# Basics of Automation Testing. VCS, CI/CD 💎
1. Automation: What? Why? When?
    - What: Using software to perform tests instead of manual execution.
    - Why: Saves time, increases efficiency, and reduces human errors.
    - When: Useful for repetitive tasks or when a quick feedback loop is needed.
    - Example: Automating login tests for a website ensures that different user credentials are validated consistently without manual repetition.

    - Advantages and Disadvantages:
      - Advantages: Faster execution, repeatability, broader test coverage.
      - Disadvantages: Initial setup time, maintenance overhead, not suitable for exploratory testing.

2. Automated Testing Processes:
    - Definition: The step-by-step activities followed in automated testing.
    - Example: In automated testing, the process might involve writing test scripts, executing them, and analyzing results. It's like teaching a computer to perform specific tests.

3. Types of Tests to Automate:
   - Definition: Deciding which tests are suitable for automation.
   - Example: Regression tests (ensuring existing features still work after changes) are often automated, as they need to be repeated frequently.
  
4. VCS (Version Control Systems):
    - Definition: Tools managing changes to source code over time.
    - Example: Git is a VCS allowing multiple developers to work on a project simultaneously. It tracks changes, enabling collaboration without conflicts.

5. CI/CD:
- CI (Continuous Integration): Regularly merging code changes into a shared repository.
- CD (Continuous Deployment/Delivery): Automatically delivering changes to production (Deployment) or preparing changes for release (Delivery).
- Example: Jenkins is a CI/CD tool that automates building, testing, and deploying code, ensuring new changes are integrated smoothly.

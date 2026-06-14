# Software Engineering

## Part 1: Quick Short Notes (Fundamentals)

### 1. Software Engineering Fundamentals
*   **Definition:** The systematic application of engineering approaches to the development, operation, and maintenance of software.
*   **Goal:** To produce high-quality software that is reliable, maintainable, meets user requirements, and is delivered on time and within budget.

### 2. SDLC (Software Development Life Cycle) Models
*   **Phases:** Requirement Analysis $\rightarrow$ Design $\rightarrow$ Implementation (Coding) $\rightarrow$ Testing $\rightarrow$ Deployment $\rightarrow$ Maintenance.
*   **Waterfall Model:** Linear and sequential. Once a phase ends, the next begins. Poor for projects with changing requirements.
*   **V-Model (Validation & Verification):** Testing phases are planned in parallel with corresponding development phases.
*   **Spiral Model:** Risk-driven model. Combines iterative nature with systematic aspects of Waterfall. Good for large, high-risk projects.
*   **Iterative & Incremental:** Develops the software in small, manageable pieces (increments), iterating over them to improve and add features.

### 3. Agile Methodology & Scrum
*   **Agile:** A set of principles focused on iterative development, continuous feedback, customer collaboration, and adapting to change over following a rigid plan.
*   **Scrum Framework:** A popular Agile implementation.
    *   *Roles:* Product Owner (represents business/customer), Scrum Master (facilitator), Development Team.
    *   *Artifacts:* Product Backlog (list of all work), Sprint Backlog (work selected for the current sprint), Increment (usable end product).
    *   *Events:* Sprints (1-4 week cycles), Daily Standup, Sprint Planning, Sprint Review, Sprint Retrospective.

### 4. Requirement Engineering
*   **Functional Requirements:** What the system *must do* (e.g., "The system shall allow users to log in").
*   **Non-Functional Requirements:** *How well* the system performs its functions (e.g., performance, security, usability, scalability).
*   **SRS Document (Software Requirement Specification):** A comprehensive document detailing all requirements, acting as an agreement between developers and clients.

### 5. Software Design
*   **Coupling:** The degree of interdependence between software modules. **Low Coupling** is highly desirable.
*   **Cohesion:** The degree to which elements inside a module belong together. **High Cohesion** is highly desirable.
*   *(Goal: High Cohesion and Low Coupling for maintainable systems).*
*   **UML (Unified Modeling Language):** Standardized visual modeling language.
    *   *Structural:* Class diagram, Object diagram.
    *   *Behavioral:* Use Case diagram, Sequence diagram, Activity diagram.

### 6. Software Testing
*   **Verification:** "Are we building the product right?" (Checking documents, code reviews, static analysis).
*   **Validation:** "Are we building the right product?" (Executing the software to ensure it meets customer needs).
*   **White Box Testing:** Internal structure, design, and code are known to the tester (e.g., Unit testing).
*   **Black Box Testing:** Internal structure is unknown; focuses on inputs and outputs (e.g., System testing).
*   **Levels of Testing:**
    1.  *Unit Testing:* Testing individual components/modules.
    2.  *Integration Testing:* Testing combined modules.
    3.  *System Testing:* Testing the complete, integrated system.
    4.  *Acceptance Testing:* Done by the end-user/client to decide whether to accept the software.

### 7. Project Management
*   **Metrics:** LOC (Lines of Code), Function Points (measure functionality from user's view).
*   **COCOMO (Constructive Cost Model):** An algorithmic software cost estimation model.
*   **Gantt Chart:** A bar chart used for project scheduling.

---

## Part 2: Placement-Related MCQs

1. Which SDLC model is highly risk-driven and incorporates prototyping iteratively?

A) Waterfall Model

B) V-Model

C) Spiral Model

D) RAD Model

**Answer:** Option **C**

**Explanation:**

The Spiral Model emphasizes risk analysis. It passes through four phases iteratively: planning, risk analysis, engineering (prototyping and development), and evaluation. It is ideal for large, complex, and expensive projects where risk mitigation is crucial.

---

2. Which of the following represents a Non-Functional Requirement?

A) The system shall calculate the total cart value.

B) The user must be able to export data to PDF.

C) The application must load the home page in under 2 seconds.

D) The admin can block a user account.

**Answer:** Option **C**

**Explanation:**

Functional requirements describe *what* the system should do (calculate, export, block). Non-functional requirements describe *how* the system behaves, specifying quality attributes such as performance, security, usability, and reliability. Loading speed is a performance metric.

---

3. For a well-designed, maintainable software system, which relationship between coupling and cohesion is desired?

A) High Coupling, High Cohesion

B) High Coupling, Low Cohesion

C) Low Coupling, Low Cohesion

D) Low Coupling, High Cohesion

**Answer:** Option **D**

**Explanation:**

Cohesion measures how closely related the functions within a single module are (we want them highly related: High Cohesion). Coupling measures the dependency between different modules (we want them highly independent: Low Coupling). Therefore, Low Coupling and High Cohesion is the ideal design.

---

4. In the Scrum framework, who is responsible for maximizing the value of the product and managing the Product Backlog?

A) The Scrum Master

B) The Product Owner

C) The Development Team

D) The Project Manager

**Answer:** Option **B**

**Explanation:**

The Product Owner represents the stakeholders and the voice of the customer. They are solely responsible for managing the Product Backlog, prioritizing features, and ensuring the development team delivers maximum business value.

---

5. "Are we building the right product?" - This question is answered during which process?

A) Verification

B) Validation

C) Refactoring

D) Compilation

**Answer:** Option **B**

**Explanation:**

Validation answers "Are we building the right product?" by checking if the software meets the user's actual needs and requirements (dynamic testing). Verification answers "Are we building the product right?" by checking if the software conforms to its specifications (document reviews, code checks).

---

6. Which testing technique relies solely on analyzing inputs and outputs without knowing the internal code structure?

A) White Box Testing

B) Glass Box Testing

C) Black Box Testing

D) Path Testing

**Answer:** Option **C**

**Explanation:**

In Black Box testing, the tester treats the software as a "black box" and is unaware of its internal logic, code, or design. They only focus on providing inputs and verifying if the outputs match the expected results.

---

7. What is the correct sequence of testing levels in software engineering?

A) Unit Testing $\rightarrow$ System Testing $\rightarrow$ Integration Testing $\rightarrow$ Acceptance Testing

B) Unit Testing $\rightarrow$ Integration Testing $\rightarrow$ System Testing $\rightarrow$ Acceptance Testing

C) Integration Testing $\rightarrow$ Unit Testing $\rightarrow$ Acceptance Testing $\rightarrow$ System Testing

D) Acceptance Testing $\rightarrow$ System Testing $\rightarrow$ Integration Testing $\rightarrow$ Unit Testing

**Answer:** Option **B**

**Explanation:**

The standard hierarchy is to first test individual components (Unit), then combine them and test their interactions (Integration), then test the software as a whole in its target environment (System), and finally have the client test it before release (Acceptance).

---

8. In Agile methodology, what is a "Sprint"?

A) A meeting held at the end of the project.

B) A document detailing all user requirements.

C) A fixed timebox (usually 1-4 weeks) during which a usable increment of the product is created.

D) The process of releasing the software to production.

**Answer:** Option **C**

**Explanation:**

A Sprint is the core heartbeat of Scrum. It is a time-boxed iteration, typically 2 to 4 weeks long, where the team works to complete a set amount of work from the backlog and deliver a potentially shippable product increment.

---

9. Which UML diagram is a structural diagram that shows the system's classes, their attributes, operations, and the relationships among objects?

A) Use Case Diagram

B) Activity Diagram

C) Sequence Diagram

D) Class Diagram

**Answer:** Option **D**

**Explanation:**

A Class Diagram is a central modeling technique in object-oriented design. It is a structural diagram that maps out the structure of a system by showing its classes, attributes, methods, and the relationships between those classes.

---

10. COCOMO is used for:

A) Software Cost Estimation

B) Software Testing

C) Software Design

D) Requirement Elicitation

**Answer:** Option **A**

**Explanation:**

COCOMO (Constructive Cost Model) is a procedural software cost estimation model developed by Barry Boehm. It uses basic regression formulas with parameters derived from historical project data to estimate the effort, cost, and schedule for a software project.

---

11. Which SDLC model is characterized by its linear, sequential flow where one phase must be completed before the next begins?

A) Agile Model

B) Iterative Model

C) Waterfall Model

D) Spiral Model

**Answer:** Option **C**

**Explanation:**

The Waterfall Model is a classic SDLC model. It is completely linear and sequential. Progress is seen as flowing steadily downwards (like a waterfall) through the phases of conception, initiation, analysis, design, construction, testing, deployment, and maintenance.

---

12. Alpha and Beta testing are forms of:

A) Unit Testing

B) Integration Testing

C) Acceptance Testing

D) System Testing

**Answer:** Option **C**

**Explanation:**

Alpha testing (done by internal employees) and Beta testing (done by real users in a real environment before official release) are both types of Acceptance Testing. They determine whether the software is ready for release to the general public.

---

13. The SRS (Software Requirement Specification) document is primarily created during which phase of the SDLC?

A) Requirement Analysis

B) Design

C) Coding

D) Testing

**Answer:** Option **A**

**Explanation:**

The Software Requirement Specification (SRS) document is the primary output of the Requirement Analysis phase. It describes the software's functional and non-functional requirements in detail, acting as a contract between developers and clients.

---

14. Which metric measures the size of a software product based on the functionalities requested by and provided to the end user?

A) Lines of Code (LOC)

B) Function Point Analysis (FPA)

C) Cyclomatic Complexity

D) Halstead's Volume

**Answer:** Option **B**

**Explanation:**

Function Point Analysis is a method to estimate the size of a software project based on the functionality delivered to the user (e.g., number of inputs, outputs, inquiries, internal files). It is independent of the programming language used, unlike LOC.

---

15. In object-oriented design, the principle of hiding the internal state and requiring all interaction to be performed through an object's methods is known as:

A) Inheritance

B) Polymorphism

C) Encapsulation

D) Abstraction

**Answer:** Option **C**

**Explanation:**

Encapsulation is the bundling of data (attributes) and methods that operate on the data into a single unit (class), and restricting direct access to some of the object's components.

---

16. Which UML diagram models the dynamic behavior of a system by showing the flow of control from one activity to another?

A) Class Diagram

B) Object Diagram

C) Activity Diagram

D) Component Diagram

**Answer:** Option **C**

**Explanation:**

An Activity diagram is a behavioral UML diagram that represents the workflow or logic of a system. It shows the flow of control from one activity to another, similar to a flowchart.

---

17. White box testing is also known as:

A) Functional Testing

B) Structural Testing

C) User Acceptance Testing

D) Beta Testing

**Answer:** Option **B**

**Explanation:**

White box testing is also called structural testing, clear box testing, or glass box testing because the tester requires an understanding of the internal structure, code, and logic of the software to design the test cases.

---

18. What is "Refactoring" in software engineering?

A) Rewriting the software from scratch in a new language.

B) Testing the software repeatedly to find bugs.

C) Improving the internal structure of existing code without changing its external behavior.

D) Adding new features to an existing software product.

**Answer:** Option **C**

**Explanation:**

Code refactoring is the process of restructuring existing computer code—changing the factoring—without changing its external behavior. It improves nonfunctional attributes of the software, making the code more readable and less complex.

---

19. Which role in Scrum acts as a facilitator for the team, removing impediments and ensuring Scrum practices are followed?

A) Product Owner

B) Developer

C) Scrum Master

D) Project Manager

**Answer:** Option **C**

**Explanation:**

The Scrum Master is responsible for ensuring the team lives agile values and principles and follows the processes and practices that the team agreed they would use. They act as a servant-leader and facilitator, protecting the team from distractions.

---

20. A Gantt chart is a tool primarily used for:

A) Risk Analysis

B) Code Review

C) Project Scheduling and Tracking

D) Database Design

**Answer:** Option **C**

**Explanation:**

A Gantt chart is a type of bar chart that illustrates a project schedule. It lists the tasks to be performed on the vertical axis, and time intervals on the horizontal axis. It is a fundamental tool for project managers to track progress against time.

# 1. Title and Student Details
**Name:** Patil Mahith Reddy  
**USN:** NB25CSE261  
**Assigned Case Study:** Question 5: Software Maintenance, Reengineering, and AI in Software Engineering  

---

# 2. Introduction
Software maintenance is the continuous process of modifying and updating a software system after its initial deployment. This phase of the software development lifecycle is essential to correct hidden faults, improve overall performance, and adapt the software to a changing technological environment. Without proper maintenance, aging systems become slow, difficult to use, and expensive to operate. 

# 3. Problem Analysis
The college's existing Student Management System is suffering from severe software aging. The primary problems identified in the legacy system are:
* **Performance Degradation:** The system has become noticeably slow, likely due to bloated databases or inefficient legacy code.
* **Obsolescence:** It contains outdated features that no longer align with current administrative workflows or modern user expectations.
* **Reliability Issues:** The system frequently produces errors, disrupting daily college operations and causing data inconsistencies.

# 4. Proposed Solution
To resolve these issues, a combination of traditional software engineering principles and modern AI-assisted tools will be applied.

### Suitable Types of Software Maintenance
* **Corrective Maintenance:** To immediately identify, isolate, and fix the bugs causing the frequent system errors.
* **Perfective Maintenance:** To optimize the code and database for faster response times, and to update the outdated features with new functionalities.
* **Adaptive Maintenance:** To ensure the modernized system is compatible with current operating systems, cloud environments, and modern web browsers.

### Steps Involved in Software Reengineering
1. **Inventory Analysis:** Evaluate the current state of the Student Management System, including its database size, active modules, and outdated components.
2. **Document Restructuring:** Create or update technical documentation to reflect how the current system operates, providing a baseline for engineers.
3. **Reverse Engineering:** Analyze the legacy codebase to extract core business rules, underlying logic, and design specifications.
4. **Code and Data Restructuring:** Clean up the existing source code and reorganize the database schemas to improve structural integrity without altering the actual functionality.
5. **Forward Engineering:** Implement the recovered design using modern programming languages, modern UI/UX frameworks, and optimized database architectures.

### Two Applications of AI in Software Engineering
1. **AI-Assisted Code Generation and Refactoring:** Tools like GitHub Copilot can be used during the restructuring phase to automatically suggest cleaner, modernized code snippets, rapidly translating legacy logic into modern frameworks.
2. **Automated Bug Detection and Testing:** AI-driven testing tools can scan the legacy system to identify patterns causing the frequent errors, and automatically generate comprehensive test cases to ensure the newly reengineered system remains stable.

### Simple Modernization Workflow Diagram

```text
+-----------------------------------+
|  Legacy Student Management System | (Slow, Outdated, Frequent Errors)
+-----------------------------------+
                 |
                 v
+-----------------------------------+
|        Reverse Engineering        | (Extract business logic & rules)
+-----------------------------------+
                 |
                 v
+-----------------------------------+      +---------------------------------+
|    Code & Data Restructuring      | <--- | AI-Assisted Code Refactoring  |
+-----------------------------------+      +---------------------------------+
                 |
                 v
+-----------------------------------+      +---------------------------------+
|        Forward Engineering        | <--- | AI Automated Bug Detection      |
+-----------------------------------+      +---------------------------------+
                 |
                 v
+-----------------------------------+
|         Modernized System         | (Fast, Reliable, Modern Features)
+-----------------------------------+

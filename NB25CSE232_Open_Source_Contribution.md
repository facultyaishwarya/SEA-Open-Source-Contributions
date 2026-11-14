# Open-Source Software Engineering

**Name:** NAMAN M METI  
**USN:** NB25CSE232  
**Assigned Case Study:** Question 4 – Open-Source Software Engineering

## 1. Introduction

Open-source software is software whose source code is publicly available. Developers can use, study, modify, and improve it according to its licence. Open-source software engineering involves developing and maintaining software through collaboration among contributors.

## 2. Problem Analysis

A group of developers is working on an open-source Library Management System hosted on GitHub. The project does not have proper documentation explaining how users can issue and return books. This may confuse users and make the system difficult to use.

## 3. Proposed Solution

A student can solve this problem by contributing a documentation file that clearly explains the book issue and return procedures.

The student can follow these steps:

1. Open the faculty's GitHub repository.
2. Click **Fork** to create a copy of the repository under the student's GitHub account.
3. Open the forked repository and navigate to the `contributions` folder.
4. Create a new Markdown file named `NB25CSE232_Open_Source_Contribution.md`.
5. Write clear instructions explaining how to issue and return books.
6. Commit the changes to the student's fork.
7. Open the **Pull requests** tab and select **New pull request** (or **Contribute → Open pull request**).
8. Check that the base repository is the faculty's repository and the head repository is the student's fork.
9. Add a suitable title and description, then click **Create pull request**.
10. The faculty reviews the contribution and merges it if it is correct.

## 4. Example Documentation

### How to Issue a Book

1. Log in to the Library Management System using your student account.
2. Search for the required book by title, author, or book ID.
3. Check whether the book is available.
4. Select the book and click **Issue Book**.
5. Confirm the issue request.
6. Check your account for the issue date and due date.

### How to Return a Book

1. Log in to the Library Management System.
2. Open the **My Issued Books** section.
3. Select the book you want to return.
4. Follow the return instructions shown by the system.
5. Confirm the return.
6. Check that the book's status is updated to **Returned**.

*Note: These are proposed user instructions. The actual button names and steps should be adjusted to match the Library Management System.*

## 5. GitHub Contribution Workflow

```text
Faculty creates repository
          |
          v
Student forks repository
          |
          v
Student creates documentation file
          |
          v
Student commits changes to the fork
          |
          v
Student creates Pull Request
          |
          v
Faculty reviews the contribution
          |
          v
Faculty merges the Pull Request
```

## 6. Benefits of Collaborative Software Development

- **Knowledge sharing:** Contributors learn from one another.
- **Improved quality:** Reviews help identify mistakes and improve documentation.
- **Teamwork:** Multiple developers can work on different parts of the project.
- **Transparency:** Changes and discussions can be viewed through GitHub.
- **Continuous improvement:** The project can be updated as new requirements arise.

## 7. Benefits and Challenges

### Benefits

- Users can understand how to issue and return books.
- Better documentation improves usability.
- The contribution helps maintain the quality of the open-source project.

### Challenges

- Understanding the existing project before editing its documentation.
- Writing instructions that are accurate and easy to follow.
- Resolving review comments or merge conflicts, if they occur.

## 8. Conclusion

Open-source software engineering encourages developers to collaborate and improve software. By forking the Library Management System repository, creating useful documentation, committing the changes, and submitting a Pull Request, the student contributes to the project in a structured way. This process also provides practical experience with GitHub and collaborative software development.

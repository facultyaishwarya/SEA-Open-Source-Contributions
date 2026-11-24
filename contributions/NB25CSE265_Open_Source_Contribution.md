# Open-Source Software Engineering: Improving Library Management System Documentation

**Student Name:** Pobbathi HariChandana\
**USN:** NB25CSE265\
**Assigned Case Study:** Q4 -- Open-Source Software Engineering\
**GitHub Filename:** `NB25CSE265_Open_Source_Contribution.md`

------------------------------------------------------------------------

## 1. Introduction

Open-source software engineering is the process of developing,
improving, and maintaining software whose source code is made publicly
available under an open-source licence. Developers and users can study
the code, suggest improvements, report bugs, and contribute changes
according to the project's contribution guidelines.

Platforms such as GitHub support this collaborative process through
repositories, branches, commits, issues, and pull requests. These tools
help contributors work independently while allowing project maintainers
to review proposed changes before they become part of the main project.

In this case study, a group of developers is maintaining an open-source
Library Management System hosted on GitHub. A student notices that the
project does not contain clear instructions explaining how users can
issue and return books. The student can help by creating or improving
the documentation and submitting the change to the project maintainers
for review.

## 2. Problem Analysis

The Library Management System lacks adequate documentation for two
important operations: issuing books and returning books. Without clear
instructions, users may not understand how to complete these tasks
correctly.

The missing documentation can lead to the following problems:

-   **User confusion:** New users may not know where to find the
    issue-book and return-book options.
-   **Incorrect usage:** Users may follow the wrong sequence of steps or
    miss required information.
-   **More support requests:** Developers and administrators may have to
    repeatedly explain basic operations.
-   **Difficult onboarding:** New users may take longer to learn the
    system.
-   **Reduced usability:** Even if the software works correctly, users
    may find it difficult to use without proper guidance.

The problem can be addressed by contributing a clear, accurate, and
easy-to-follow documentation file to the open-source repository.

## 3. Proposed Solution

The student should prepare a documentation file describing the
procedures for issuing and returning books. The document should use
simple language, numbered steps, and clear section headings.

### 3.1 Suggested documentation content

The student can create a file such as `Book_Issue_and_Return_Guide.md`
inside the project's documentation folder.

**A. How to issue a book**

1.  Open the Library Management System and sign in using an authorized
    account.
2.  Navigate to the book issue or circulation section.
3.  Search for the required book using its title, author, or book ID.
4.  Check whether the book is available for issue.
5.  Select the eligible library member or enter the required member ID.
6.  Confirm the issue operation.
7.  Verify that the system displays the issue details and due date.

**B. How to return a book**

1.  Sign in to the Library Management System.
2.  Navigate to the book return section.
3.  Search for the issued book or the member's issue record.
4.  Verify the book and issue details.
5.  Select the return option and confirm the operation.
6.  Check whether the system displays any overdue information or
    applicable fine.
7.  Verify that the book's status has been updated to available, if no
    other restriction applies.

*Note:* These are general user-guide steps proposed for the case study.
Before merging the documentation, the contributor should compare them
with the actual application's screens, terminology, permissions, and
behaviour. Any step that does not match the implementation should be
corrected.

### 3.2 GitHub contribution workflow

The student can contribute the documentation by following these steps:

1.  **Find the repository:** Open the Library Management System
    repository on GitHub and read its README and contribution
    guidelines.
2.  **Fork the repository:** Click **Fork** to create a copy of the
    repository under the student's GitHub account. The original
    repository remains unchanged.
3.  **Clone the fork (if working locally):** Copy the fork's repository
    URL and use `git clone` to download it to the computer.
    Alternatively, a permitted GitHub web editor can be used.
4.  **Create a branch:** Create a separate branch, for example,
    `documentation-book-issue-return`. A branch keeps the proposed work
    separate from the main branch.
5.  **Create or update the documentation:** Add
    `Book_Issue_and_Return_Guide.md` in the appropriate documentation
    folder. Explain the issue and return procedures clearly and check
    that the content matches the application.
6.  **Review the changes:** Check spelling, headings, links, Markdown
    formatting, and technical accuracy. Preview the Markdown if
    possible.
7.  **Commit the changes:** Save the work as a commit with a meaningful
    message, such as `Add book issue and return user guide`.
8.  **Push the branch:** If working locally, push the branch to the
    student's fork on GitHub.
9.  **Create a Pull Request:** Open the fork on GitHub and select
    **Contribute** or **Compare & pull request**. Set the original
    project repository and its target branch as the base, and the
    student's fork and contribution branch as the compare/head.
10. **Describe the Pull Request:** Use a clear title, such as
    `Add documentation for issuing and returning books`. In the
    description, explain what was added and why it is useful.
11. **Respond to review:** The project maintainer reviews the changes
    and may request corrections. The student should make the requested
    updates and commit them to the same branch.
12. **Merge:** Once the maintainer approves the contribution, the
    maintainer can merge the Pull Request into the original repository.

### 3.3 GitHub contribution workflow diagram

``` mermaid
flowchart TD
    A[Open the original GitHub repository] --> B[Read README and contribution guidelines]
    B --> C[Fork the repository]
    C --> D[Create a contribution branch]
    D --> E[Create or update the documentation]
    E --> F[Review and verify the changes]
    F --> G[Commit the changes]
    G --> H[Push the branch to the fork]
    H --> I[Create a Pull Request to the original repository]
    I --> J[Maintainer reviews the Pull Request]
    J --> K{Changes approved?}
    K -- No: changes requested --> L[Make corrections and commit again]
    L --> H
    K -- Yes --> M[Maintainer merges the Pull Request]
    M --> N[Documentation is added to the main project]
```

## 4. Importance of Contributing to Open-Source Projects

Contributing to open-source projects is valuable for both the project
and the contributor.

-   **Improves software quality:** Contributions can fix problems,
    improve features, and make documentation more complete.
-   **Helps the community:** A useful improvement can benefit many
    users, not just the person who suggested it.
-   **Encourages collaboration:** Contributors learn to communicate with
    maintainers, discuss issues, and review changes.
-   **Builds practical skills:** Students gain experience with Git,
    GitHub, Markdown, version control, and software project workflows.
-   **Promotes transparency:** Public discussions and review histories
    make changes easier to understand and track.
-   **Supports continuous improvement:** Different contributors can
    improve the project over time.

## 5. Benefits and Challenges

### 5.1 Benefits of the proposed contribution

1.  **Better user experience:** Users can follow clear instructions to
    issue and return books.
2.  **Fewer mistakes:** Step-by-step guidance can reduce confusion and
    incorrect operations.
3.  **Reduced support effort:** Administrators and developers may
    receive fewer repetitive questions.
4.  **Easier onboarding:** New users can learn the library system more
    quickly.
5.  **Improved project quality:** Complete documentation makes the
    project more understandable and maintainable.

### 5.2 Challenges

1.  **Understanding the existing application:** The contributor must
    inspect the system to ensure the instructions match its actual
    workflow.
2.  **Following project standards:** The documentation must follow the
    repository's naming, formatting, and contribution guidelines.
3.  **Review and feedback:** Maintainers may request changes, so the
    contributor must understand and address review comments.
4.  **Keeping documentation updated:** Future software changes may make
    some instructions outdated.

These challenges can be managed by reading the project guidelines,
testing the described steps where possible, using clear Markdown, and
updating the document when the application changes.

## 6. Commit and Pull Request Details

The following are suitable details for the proposed contribution:

  -----------------------------------------------------------------------------------------
  Item                                Suggested value
  ----------------------------------- -----------------------------------------------------
  Contribution type                   Documentation improvement

  File to add                         `Book_Issue_and_Return_Guide.md`

  Suggested branch                    `documentation-book-issue-return`

  Commit message                      `Add book issue and return user guide`

  Pull Request title                  `Add documentation for issuing and returning books`

  Target                              Original Library Management System repository
  -----------------------------------------------------------------------------------------

The Pull Request should briefly state that the contribution adds user
instructions for issuing and returning books. The student should include
the actual Pull Request URL in the submitted evidence after creating it.
A URL must not be invented or reported before the Pull Request exists.

## 7. Conclusion

Open-source software engineering allows developers and students to work
together to improve software projects. In the given Library Management
System case study, the lack of instructions for issuing and returning
books can make the system difficult for users to understand. The student
can solve this problem by preparing accurate, step-by-step documentation
and contributing it through GitHub.

The process involves forking the original repository, creating a branch,
adding or modifying the documentation, committing the changes, and
submitting a Pull Request. The project maintainer reviews the
contribution and merges it after approval. This process improves the
project's documentation while helping the student gain practical
experience in version control and collaborative software development.

## 8. Submission Evidence

Complete the following after performing the contribution on GitHub:

-   **Original repository URL:** Add the faculty/project repository URL.
-   **Student fork URL:** Add the URL of your fork.
-   **Pull Request URL:** Add the actual Pull Request URL.
-   **Merge status:** Record whether the Pull Request is pending,
    approved, or merged.

**Student:** Pobbathi HariChandana\
**USN:** NB25CSE265

Name:Nabeel Ahmed 
USN:NB25CSE227

# Question 3: DevOps Practices and CI/CD Pipelines

## 1. Introduction to DevOps

DevOps is a software development approach that combines Development (Dev) and Operations (Ops) teams to develop, test, and deliver software faster.

It focuses on automation, teamwork, and continuous improvement.

In an online shopping application, DevOps helps developers introduce new features and fix bugs quickly without delaying the application.

## 2. Meaning of CI and CD

### Continuous Integration (CI)
- Developers frequently add their code changes to a shared repository.
- The code is automatically built and tested.
- Errors are identified and fixed early.

### Continuous Delivery/Deployment (CD)
- Continuous Delivery automatically prepares tested code for release.
- Continuous Deployment automatically releases tested code into the production environment without manual approval.

## 3. CI/CD Pipeline Stages

The following stages are involved in a CI/CD pipeline:

1. **Code:** Developers write and upload code to a shared repository like GitHub.

2. **Build:** The system automatically compiles the code and creates a software package.

3. **Test:** Automated tests are performed to identify bugs and errors.

4. **Release:** The tested application is prepared for deployment.

5. **Deploy:** The application is automatically deployed to the production server.

6. **Monitor:** The application is continuously monitored to identify errors and performance issues.

## 4. Explanation of Build, Test, and Deployment

- **Build:** Converts the source code into an executable application.
- **Test:** Checks whether the application works correctly and is free from errors.
- **Deployment:** Makes the updated application available to users.

## 5. Benefits of Automation (Any Three)

1. **Saves Time:** Automation reduces manual work and speeds up software development.

2. **Reduces Errors:** Automated testing helps identify bugs and reduces human mistakes.

3. **Faster Delivery:** New features and bug fixes can be released quickly to customers.

## 6. CI/CD Pipeline Diagram

```text
       +------------------+
       |       CODE       |
       | Developer writes |
       |      code        |
       +------------------+
                |
                v
       +------------------+
       |      BUILD       |
       | Build application|
       +------------------+
                |
                v
       +------------------+
       |       TEST       |
       | Automated testing|
       +------------------+
                |
                v
       +------------------+
       |      RELEASE     |
       | Prepare software |
       +------------------+
                |
                v
       +------------------+
       |      DEPLOY      |
       | Deploy to server |
       +------------------+
                |
                v
       +------------------+
       |     MONITOR      |
       | Check performance|
       +------------------+
                |
                v
       Continuous Feedback
```

## Conclusion

DevOps and CI/CD pipelines help software companies automate building, testing, and deployment. They reduce errors, save time, and ensure faster delivery of reliable software to customers.

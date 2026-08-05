# Day 33 – Introduction to Maven

## Overview

Today I started learning **Apache Maven**, one of the most popular build automation and project management tools used in Java-based applications.

I learned why Maven is used, its lifecycle, how to install Maven and Java on both Windows and Linux (AWS EC2), and performed hands-on practice by cloning my GitHub repository and executing Maven lifecycle commands.

---

## What is Maven?

Apache Maven is a **Build Automation and Project Management Tool** primarily used for Java projects.

It helps developers automate tasks such as:

- Compiling source code
- Managing project dependencies
- Running tests
- Packaging applications
- Deploying applications

---

## Why is Maven Used?

- Automates the build process
- Manages project dependencies
- Provides a standard project structure
- Simplifies project management
- Supports plugins for additional functionality
- Makes builds consistent across different environments

---

## Maven Lifecycle

Maven follows a predefined build lifecycle.

### 1. Validate
Checks whether the project structure is correct.

```bash
mvn validate
```

### 2. Compile

Compiles the source code.

```bash
mvn compile
```

### 3. Test

Runs unit test cases.

```bash
mvn test
```

### 4. Package

Packages the application into a JAR or WAR file.

```bash
mvn package
```

### 5. Verify

Runs quality checks and verifies the package.

```bash
mvn verify
```

### 6. Install

Installs the package into the local Maven repository.

```bash
mvn install
```

### 7. Deploy

Deploys the package to a remote repository.

```bash
mvn deploy
```

---

## Installing Java and Maven on Windows

Learned how to:

- Install Java (JDK)
- Configure JAVA_HOME
- Install Apache Maven
- Configure MAVEN_HOME
- Update Environment Variables
- Verify installation

Commands used:

```bash
java -version

mvn -version
```

---

## Installing Java and Maven on AWS EC2 (Linux)

Installed Java:

```bash
sudo yum install java-17-amazon-corretto -y
```

Installed Maven:

```bash
sudo yum install maven -y
```

Verified installation:

```bash
java -version

mvn -version
```

---

## Hands-on Practice

Today's practical activities included:

- Installed Java on Windows
- Installed Maven on Windows
- Installed Java on AWS EC2
- Installed Maven on AWS EC2
- Cloned my GitHub repository into the Linux machine
- Copied my Maven project from local to GitHub
- Executed different Maven lifecycle commands
- Verified successful project build using Maven

---

## What I Learned

- What is Maven
- Why Maven is used
- Maven Build Lifecycle
- Installing Java
- Installing Maven
- Configuring Java and Maven
- Maven lifecycle commands
- Cloning GitHub repository into Linux
- Building projects using Maven
- Hands-on practice with Maven on Windows and Linux

---

## Key Takeaway

Maven simplifies Java project development by automating builds, managing dependencies, and providing a standard project structure. Understanding the Maven lifecycle is an essential skill for Java developers and DevOps engineers working with CI/CD pipelines.

---


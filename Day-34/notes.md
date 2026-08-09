# Day 34 – Apache Tomcat & Hosting a Java Application

## Overview

Today I continued my learning about application hosting.

In the previous session, I learned how to use Maven to build a Java project and generate a package. Today I learned how to use **Apache Tomcat** to host that packaged Java web application.

---

## What is Apache Tomcat?

Apache Tomcat is an open-source web server and **Servlet/JSP container** used to run Java-based web applications.

Tomcat can deploy Java web applications packaged as **WAR (Web Application Archive)** files.

---

## Why is Apache Tomcat Used?

Apache Tomcat is used to:

- Host Java web applications
- Run Servlet and JSP-based applications
- Deploy WAR files
- Provide a runtime environment for Java web applications
- Test and run applications on a server

---

## Installing Apache Tomcat

Learned the basic steps involved in installing Apache Tomcat on a Linux server.

### Step 1 – Download Apache Tomcat

Download the required Tomcat version from the official Apache Tomcat website.

### Step 2 – Extract Tomcat

Extract the downloaded Tomcat archive into the required directory.

### Step 3 – Start Tomcat

Navigate to the Tomcat `bin` directory and start the server.

```bash
./startup.sh

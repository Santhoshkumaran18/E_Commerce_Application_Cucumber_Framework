# 🛒 OpenCart E-Commerce Automation Framework

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Cucumber](https://img.shields.io/badge/Cucumber-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)

---

## 📌 Project Overview

This project automates key user workflows of the **OpenCart E-Commerce Application** using **Cucumber (BDD)**, **Selenium WebDriver**, **JUnit/TestNG**, and **Page Object Model (POM)**. It is designed to support **cross-browser testing**, **data-driven testing**, **logging**, and **reporting**.

---

## 🚀 Tech Stack

- **Language**: Java  
- **Automation Tool**: Selenium WebDriver  
- **BDD Framework**: Cucumber  
- **Build Tool**: Maven  
- **Unit Test Framework**: JUnit 4  
- **Reporting**: Extent Reports  
- **Logging**: Log4j2  
- **Excel Reading**: Apache POI  
- **Data Generation**: Java Faker  
- **Browser Driver Management**: WebDriverManager  

---

## 📁 Folder Structure

```bash
E_Commerce_Application_Cucumber
├── src
│   └── test
│       ├── java
│       │   ├── factory              # Base setup (WebDriver, config)
│       │   ├── hooks                # Cucumber Hooks (Before/After)
│       │   ├── pageObjects          # Page Object Model classes
│       │   ├── stepDefinitions      # Step definitions for feature files
│       │   ├── testRunner           # TestRunner class
│       │   └── utilities            # DataReader, reusable utils
│       └── resources
│           ├── config.properties    # Config (URL, browser, etc.)
│           ├── extent.properties    # Extent config
│           └── log4j2.xml           # Logging configuration
├── Features                        # All .feature files
├── logs                            # Log files
├── reports                         # HTML reports
├── screenshots                     # Failed test screenshots
├── testData                        # Excel files for DDT
├── pom.xml                         # Maven configuration
└── README.md

---

## **How to Run the Tests**

### **💡 Prerequisites**
- **Java 8 or above**
- **Maven** installed
- **Chrome/Edge/Firefox** installed
- **IDE** (like Eclipse or IntelliJ)

---

### **🛠️ Run from IDE**
1. Open the project in Eclipse/IntelliJ
2. Navigate to `TestRunner.java`
3. Right-click and choose **Run as JUnit Test**

---

**### ▶️ Run from Command Line**
```bash
mvn clean test
```

## 🔧 Configuration
1. Update `config.properties` inside `src/test/resources`:

```properties
browser=chrome
url=https://demo.opencart.com](https://tutorialsninja.com/demo/index.php?route=common/home
```

## ✅ Features Implemented
- User Registration
- User Login (with Data-Driven Testing)
- Product Search
- Add to Cart
- Checkout Page Validation

## 📊 Reports & Logs
- **Reports:** Available under `reports/myreport.html`
- **Logs:** Generated in `logs/` folder
- **Screenshots:** Captured on failure and stored in `screenshots/`

## 📘 Sample Feature File
```gherkin
Feature: User Login Feature

  Scenario Outline: Successful login with valid credentials
    Given User launches the application
    When User navigates to Login page
    And User enters email "<email>" and password "<password>"
    Then User should be navigated to MyAccount Page

  Examples:
    | email              | password  |
    | test1@email.com    | pass123   |
    | test2@email.com    | pass456   |
```

## 🧰 Utilities Used
- **DataReader.java:** Reads Excel data for Data-Driven Testing (DDT)
- **Hooks.java:** Manages browser setup and teardown
- **BaseClass.java:** WebDriver initialization
- **Java Faker:** Random test data generation

## 🤝 Contribution Guidelines
1. Fork the repository
2. Create your feature branch:
   ```bash
   git checkout -b feature/featureName
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/featureName
   ```
5. Open a Pull Request

## 📝 License
This project is licensed under the **MIT License**.

## 📷 Screenshots

**Cucumber Report**
![image](https://github.com/user-attachments/assets/2c9a4e25-aa30-4b7b-840e-d1c3bfc1b1f7)

## 🙋‍♂️ Contact
For queries or collaborations, feel free to reach out via **GitHub Issues** or email.

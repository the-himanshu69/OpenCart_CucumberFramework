
# OpenCart Cucumber Hybrid Framework

This is a **custom-built hybrid framework** developed for automating the testing of the OpenCart e-commerce platform. It uniquely blends **Data-Driven Testing (DDT)** with **Behavior Driven Development (BDD) using Cucumber**, enabling a highly maintainable and modular test automation solution.


## Project Highlights

- **Hybrid Architecture**

        Data-Driven Testing (DDT): Leverages external data sources, such as Excel, to run tests with various input combinations. The LoginDDTExcel.feature demonstrates dynamic test execution based on login credentials provided in an Excel sheet, allowing efficient handling of large datasets.

        Page Object Model (POM): The framework's modular structure abstracts UI interactions, ensuring that test scripts are clean, concise, and easy to maintain.

        Cucumber Integration: Using **Gherkin syntax**, the framework bridges the gap between technical teams and business stakeholders by writing test cases in a natural language format.

- **Advanced Logging and Reporting**

        Log4j2 integration: This project goes beyond basic logging, ensuring comprehensive coverage of each test scenario, including timestamps, step-wise execution, and debugging insights.

        Customizable Reports: HTML reports generated using ExtentReports come with enhanced filtering options and visual representation of test results, including screenshots on failure.

- **Modular TestData Management**

        A dedicated testData folder with an Excel-driven approach allows easy modification and extension of test data without altering the code.


## Unique Technical Implementations

- Reusable Utility Classes: The utilities package is optimized to contain frequently used functions such as WebDriver initialization, waiting mechanisms, and data handling utilities.

- Custom Configurations: The config.properties file is fine-tuned for flexible environment management, allowing the framework to switch between different browsers and environments with minimal changes.


## Folder Structure Overview

- **src/test/java**:

        factory: Handles WebDriver initialization with multi-browser support.

        pageObjects: Encapsulates page-specific actions to keep tests clean.

        stepDefinitions: Contains logic that connects Gherkin steps to Java code.

        testRunner: Executes the test scenarios with parallel execution support.

        utilities: Provides reusable functions like reading Excel data, interacting with web elements, and handling timeouts.

- **src/test/resources**:

        config.properties: Central configuration file for environment and browser setup.

        extent.properties: Manages report settings.

        log4j2.xml: Log4j2 setup for controlling log levels and output formats.

- **Features**:

        Login.feature: Multiple login scenarios including valid, invalid, and blocked users.

        LoginDDTExcel.feature: Parameterized login tests using Excel data.

        Registration.feature: Covers both successful and failed registrations.
        
- **testData**:
        
        Stores the Excel sheet Opencart_LoginData.xlsx used for dynamic data input during tests.

- **reports**:

        Generated test execution reports (HTML format) for easy analysis.


## Tools & Technologies

- **Java (JDK 1.8)**: Core programming language.
- **Maven**: For dependency management and build automation.
- **Cucumber**: BDD framework using Gherkin syntax.
- **Selenium WebDriver**: Browser automation tool.
- **TestNG**: Testing framework to manage test execution.
- **Log4j2**: Logging framework.
- **ExtentReports**: Custom HTML reports.
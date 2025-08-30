# BookMyShow Automation Framework

## Overview

This project is a Selenium, Cucumber, and TestNG based automation framework for testing the BookMyShow web application. It supports cross-browser testing, BDD with Cucumber, data-driven testing, and integrates with Git and Jenkins for CI/CD. The framework is modular, maintainable, and designed for collaborative teams.

---

## Features

- **WebDriver Setup:** Automated browser driver management for Chrome and Edge.
- **Page Object Model (POM):** Modular page classes for maintainability.
- **Cucumber BDD:** Gherkin-based feature files for business-readable scenarios.
- **TestNG Integration:** Test execution and reporting.
- **Explicit/Fluent Waits:** Robust handling of dynamic elements.
- **Data-Driven Testing:** Excel and properties file support.
- **Exception Handling:** Graceful error management.
- **Screenshot Capture:** Automatic screenshots on test failures.
- **Cucumber HTML/JSON Reports:** Detailed reporting after each run.
- **Git Integration:** Version control for team collaboration.
- **Jenkins Integration:** Automated CI/CD pipeline.

---

## Project Structure

```
.
├── pom.xml
├── testng.xml
├── config/
│   └── config.properties
├── features/
│   ├── city.feature
│   ├── giftcard.feature
│   ├── login.feature
│   └── movie.feature
├── reports/
│   ├── cucumber.html
│   └── cucumber.json
├── screenshots/
│   └── *.png
├── src/
│   ├── main/
│   │   └── java/
│   └── test/
├── target/
│   └── ...
├── test-output/
│   └── ...
```

---

## Getting Started

### Prerequisites

- Java 17+
- Maven 3.6+
- Chrome and/or Edge browsers
- [Git](https://git-scm.com/)
- [Jenkins](https://jenkins.io/) (optional, for CI/CD)

### Setup

1. **Install dependencies:**
   ```sh
   mvn clean install
   ```

2. **Configure properties:**
   - Update `config/config.properties` for environment-specific settings.

3. **Test Data:**
   - Place your Excel test data in the appropriate directory if required.

---

## Running Tests

### Using TestNG

- **All Browsers:**
  ```sh
  mvn test
  ```
- **Specific Browser:**
  Edit [`testng.xml`](testng.xml) and set the desired browser parameter (`chrome`, `edge`).

### Using Jenkins

- Configure a Jenkins job to pull from your Git repository and run:
  ```sh
  mvn clean test
  ```
- Publish `reports/cucumber.html` as a build artifact.

---

## Reporting

- **HTML & JSON Reports:** Generated in the `reports/` directory after each run.
- **Screenshots:** Captured on failures and saved in the `screenshots/` directory.

---

## Data-Driven Testing

- Test data is managed via Excel and properties files.
- Utilities in `src/main/java/utils/ExcelUtils.java` handle data extraction.

---

## Contribution

- Fork the repository and create a feature branch.
- Raise a pull request for review.

---

## License

This project is for educational and demonstration purposes.

---

## Authors

- Deekshith Bokka

---

## References

- [Selenium Documentation](https://www.selenium.dev/documentation/)
- [Cucumber Documentation](https://cucumber.io/docs/)
- [TestNG Documentation](https://testng.org/doc/)
- [Jenkins Documentation](https://www.jenkins.io/doc/)

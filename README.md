# OpenCart Testing Project

## Project Overview

This project provides comprehensive testing coverage for the OpenCart e-commerce platform, including Manual Testing, Automation Testing, Database Testing, and API Testing. The testing suite ensures the reliability, functionality, and performance of the OpenCart application across multiple layers.

## Table of Contents

- [Project Structure](#project-structure)
- [Testing Modules](#testing-modules)
  - [Manual Testing](#manual-testing)
  - [Automation Testing](#automation-testing)
  - [Database Testing](#database-testing)
  - [API Testing](#api-testing)
- [Prerequisites](#prerequisites)
- [Installation and Setup](#installation-and-setup)
- [Running Tests](#running-tests)
- [Test Reports](#test-reports)
- [Team Members](#team-members)
- [Contributing](#contributing)

## Project Structure

```
Final-Depi/
├── Manual/                  # Manual test cases and bug reports
│   ├── readme.md
│   └── Test Cases/         # Excel files with test cases and bug reports
├── Automation/             # Selenium-based automation framework
│   ├── src/
│   │   └── test/
│   │       └── java/
│   │           └── org/
│   │               └── example/
│   ├── pom.xml
│   ├── testng.xml
│   └── readme.md
├── Database/               # Database testing scripts
│   ├── DB_Testing.sql
│   └── readme.md
├── API/                    # API testing collections
│   ├── OpenCart_API_Testing.json
│   └── readme.md
└── README.md
```

## Testing Modules

### Manual Testing

The Manual Testing module contains comprehensive test cases covering various OpenCart features:

#### Test Coverage Areas:
- **User Authentication**: Registration, Login, Logout, and Password Recovery
- **Product Management**: Product Display, Product Comparison, Search Functionality
- **Shopping Experience**: Shopping Cart, Wish List, Checkout Process
- **Account Management**: My Account section, Order History
- **UI Elements**: Footer Navigation, Currency Selection
- **Downloads**: Digital Product Downloads

#### Deliverables:
- Detailed test cases in Excel format
- Bug reports with severity classification
- Test execution results

#### Team Members:
- Osama Mohamed Ahmed Elkady - Login/Logout, Shopping Cart, Footer, Search
- Hassan Mohamed Kandil - Register, Product Display Page, Wish List, Currencies
- Mahmoud Ahmed Shahat - Forget Password, Product Compare, My Account, Download
- Malak Abdelmoniem Elsaid - Additional Manual Testing Support

### Automation Testing

Automated test suite built using Selenium WebDriver, TestNG, and Maven.

#### Technology Stack:
- **Framework**: Selenium WebDriver 4.x
- **Build Tool**: Apache Maven
- **Testing Framework**: TestNG
- **Language**: Java
- **Design Pattern**: Page Object Model (POM)

#### Test Cases Implemented:
- TestCase01: Register User
- TestCase02: Login User with Correct Email and Password
- TestCase03: Login User with Incorrect Email and Password
- TestCase04: Logout User
- TestCase10: Verify Subscription in Home Page
- TestCase11: Verify Subscription in Cart Page
- Additional test cases covering various user workflows

#### Key Features:
- Modular and reusable test components
- BaseTest class for common setup and teardown operations
- Comprehensive test reporting with TestNG
- Cross-browser testing support
- Parallel test execution capability

#### Team Member:
- Elhussieny Sabry Elshahat

### Database Testing

Database testing ensures data integrity, validation, and proper storage/retrieval operations.

#### Testing Focus:
- Data Integrity Validation
- CRUD Operations Testing
- Database Schema Validation
- Query Performance Testing
- Stored Procedures and Functions Testing
- Data Consistency Checks

#### Deliverables:
- SQL test scripts
- Database test scenarios
- Data validation queries

#### Team Member:
- Elhussieny Sabry Elshahat

### API Testing

API testing validates the backend services and RESTful APIs of OpenCart.

#### Testing Approach:
- RESTful API endpoint validation
- Request/Response verification
- Status code validation
- Authentication and Authorization testing
- Error handling validation
- Performance testing

#### Tools Used:
- Postman Collection (JSON format)
- API request/response documentation

#### Team Member:
- Mohamed Mahmoud Aboelnasr

## Prerequisites

### For Manual Testing:
- Microsoft Excel or compatible spreadsheet application
- Access to OpenCart test environment

### For Automation Testing:
- Java Development Kit (JDK) 8 or higher
- Apache Maven 3.6 or higher
- Chrome/Firefox browser
- ChromeDriver/GeckoDriver (compatible with browser version)
- IDE (IntelliJ IDEA, Eclipse, or VS Code)

### For Database Testing:
- MySQL or compatible database server
- Database client (MySQL Workbench, DBeaver, etc.)
- Access credentials to OpenCart database

### For API Testing:
- Postman application
- OpenCart API credentials

## Installation and Setup

### Setting Up Automation Tests:

1. Clone the repository:
```bash
git clone https://github.com/elhussienysabry/Opencart-testing.git
cd Final-Depi/Automation
```

2. Install dependencies:
```bash
mvn clean install
```

3. Configure test parameters:
   - Update browser settings in `BaseTest.java`
   - Configure application URL and credentials as needed

### Setting Up Database Tests:

1. Navigate to Database folder:
```bash
cd Database
```

2. Connect to your MySQL database:
```bash
mysql -u username -p database_name
```

3. Execute test scripts:
```bash
source DB_Testing.sql
```

### Setting Up API Tests:

1. Install Postman application
2. Import the collection:
   - Open Postman
   - Click Import
   - Select `API/OpenCart_API_Testing.json`
3. Configure environment variables if needed

## Running Tests

### Running Automation Tests:

Execute all tests:
```bash
cd Automation
mvn test
```

Execute specific test:
```bash
mvn test -Dtest=TestCase01_RegisterUser
```

Execute tests using TestNG XML:
```bash
mvn test -DsuiteXmlFile=testng.xml
```

### Running Manual Tests:
1. Open the respective Excel file from the `Manual` folder
2. Follow the test steps documented
3. Record results and any defects found

### Running Database Tests:
```bash
mysql -u username -p database_name < Database/DB_Testing.sql
```

### Running API Tests:
1. Open Postman
2. Select the imported collection
3. Run individual requests or entire collection
4. Review response data and status codes

## Test Reports

### Automation Test Reports:

After test execution, reports are generated in:
- **TestNG HTML Report**: `Automation/target/surefire-reports/index.html`
- **TestNG XML Report**: `Automation/target/surefire-reports/testng-results.xml`
- **Emailable Report**: `Automation/target/surefire-reports/emailable-report.html`

Open the HTML reports in any web browser to view detailed test results, including:
- Test execution summary
- Pass/Fail status for each test
- Execution time
- Error messages and stack traces for failed tests

### Manual Test Reports:
- Test execution results documented in Excel files
- Bug reports with screenshots and severity levels
- Located in respective team member folders under `Manual/`

### API Test Reports:
- Available through Postman Test Runner
- Export results for documentation

## Team Members

### Manual Testing Team:
- **Osama Mohamed Ahmed Elkady** - Login/Logout, Shopping Cart, Footer, Search
- **Hassan Mohamed Kandil** - Register, Product Display Page, Wish List, Currencies
- **Mahmoud Ahmed Shahat** - Forget Password, Product Compare, My Account, Download
- **Malak Abdelmoniem Elsaid** - Manual Testing Support

### Automation Testing:
- **Elhussieny Sabry Elshahat** - Selenium Test Automation Framework

### Database Testing:
- **Elhussieny Sabry Elshahat** - Database Validation and Testing

### API Testing:
- **Mohamed Mahmoud Aboelnasr** - API Test Suite Development

## Contributing

To contribute to this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## Best Practices

- Follow the existing code structure and naming conventions
- Write clear and descriptive test case names
- Document any new test scenarios added
- Update README when adding new features or test cases
- Ensure all tests pass before committing changes
- Review and maintain test data regularly

## Troubleshooting

### Common Issues:

**Automation Tests:**
- If tests fail due to browser driver issues, ensure ChromeDriver/GeckoDriver matches your browser version
- Check that the application URL is accessible
- Verify Java and Maven are properly installed

**Database Tests:**
- Ensure database credentials are correct
- Check database server is running
- Verify user has necessary permissions

**API Tests:**
- Confirm API endpoints are accessible
- Check authentication tokens are valid
- Verify network connectivity

## License

This project is developed for educational and testing purposes.

## Contact

For questions or support, please contact the respective team members or create an issue in the repository.

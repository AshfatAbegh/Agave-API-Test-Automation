# Agave-API-Test-Automation

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![REST Assured](https://img.shields.io/badge/REST%20Assured-Success-green?style=for-the-badge)

## Overview

Agave is a Japanese company specializing in providing a wide selection of small houseplants through a mobile application, complemented by an admin portal for management purposes. 

This repository is dedicated to **API test automation** using RestAssured, providing comprehensive coverage of all HTTP methods—GET, POST, PUT, DELETE—for API testing. The framework is built with modern testing practices and best practices in automation engineering.

## Key Features

✅ **Test Frameworks**: Leveraging both TestNG and JUnit for test execution, enabling structured assertions and detailed validation of API responses.

✅ **JSON Schema Validation**: Ensures that the API responses conform to the expected structure, improving reliability and consistency in testing.

✅ **Comprehensive API Coverage**: Automates the testing of all common API requests, ensuring full lifecycle testing from request to response.

✅ **Reporting**: Integrated with the Maven Surefire Plugin for generating test reports, with additional support for Surefire TestNG Reports to provide clear, actionable insights into test outcomes.

✅ **CI/CD Ready**: Tailored for seamless integration into CI/CD pipelines, ensuring reliable API test automation in modern development workflows.

## Technology Stack

- **Language**: Java
- **API Testing Framework**: RestAssured
- **Test Runners**: TestNG, JUnit
- **Build Tool**: Maven
- **Reporting**: Maven Surefire Plugin
- **Schema Validation**: JSON Schema

## Project Structure

```
Agave-API-Test-Automation/
├── src/
│   ├── main/
│   │   └── java/
│   └── test/
│       └── java/
├── tests/
├── pom.xml
└── README.md
```

## Prerequisites

- Java 8 or higher
- Maven 3.6+
- Git

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/AshfatAbegh/Agave-API-Test-Automation.git
cd Agave-API-Test-Automation
```

### 2. Install Dependencies

```bash
mvn clean install
```

### 3. Run Tests

Execute all tests:
```bash
mvn test
```

Run specific test class:
```bash
mvn test -Dtest=TestClassName
```

Run tests with TestNG:
```bash
mvn test -Dgroups="smoke" -Dexcludes="**/integration/**"
```

## Test Execution & Reporting

After running tests, reports are generated in:
- **Surefire Reports**: `target/surefire-reports/`
- **TestNG Reports**: `test-output/`

View HTML test reports:
```bash
open target/surefire-reports/index.html
```

## API Testing Coverage

This framework provides automated testing for:

| HTTP Method | Coverage | Status |
|-----------|----------|--------|
| GET | Read operations | ✅ Complete |
| POST | Create operations | ✅ Complete |
| PUT | Update operations | ✅ Complete |
| DELETE | Delete operations | ✅ Complete |

## JSON Schema Validation

All API responses are validated against predefined JSON schemas to ensure:
- Correct data structure
- Valid data types
- Required fields presence
- Response consistency

## CI/CD Integration

This project is ready for integration with popular CI/CD platforms:
- GitHub Actions
- Jenkins
- GitLab CI/CD
- CircleCI

Example GitHub Actions workflow:
```yaml
name: API Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-java@v2
        with:
          java-version: '11'
      - run: mvn clean test
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Best Practices

- Write meaningful test names that describe what is being tested
- Use data-driven tests for multiple scenarios
- Maintain clear separation between test data and test logic
- Follow the AAA pattern: Arrange, Act, Assert
- Keep test dependencies minimal and isolated
- Document complex test scenarios

## Troubleshooting

### Build Failures
```bash
mvn clean install -X
```

### Dependency Issues
```bash
mvn dependency:resolve
mvn dependency:tree
```

### Test Execution Issues
Ensure Java version matches the project requirements:
```bash
java -version
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact & Support

For questions, issues, or suggestions, please create an issue on the [GitHub Issues](https://github.com/AshfatAbegh/Agave-API-Test-Automation/issues) page.

**Author**: [@AshfatAbegh](https://github.com/AshfatAbegh)

---

**Last Updated**: 2026-05-06

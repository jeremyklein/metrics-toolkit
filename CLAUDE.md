# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands
- Build: `mvn clean install`
- Run all tests: `mvn test`
- Run single test: `mvn test -Dtest=TestFileName.xml#test-name`
- Generate coverage report: `mvn coverage-report`

## Runtime Environment
- Mule Runtime: 4.6.0
- Java Version: 17
- Maven Plugin: 3.8.0

## Code Style Guidelines
- **XML Config**: Use doc:id and doc:name attributes for documentation
- **DataWeave**: Use explicit output types (e.g., `output application/json`)
- **Variables**: Use camelCase for variable names
- **Error Handling**: Follow APIKit pattern in src/main/resources/dw/apikit/
- **File Naming**: Follow existing patterns (collector-*.xml, loader-*.xml)
- **Security**: Store sensitive data using Secure Properties Module
- **Testing**: Create mock responses for API calls and verify expected outputs

## Main Components
- Collectors: gather metrics from various sources
- Aggregators: process and combine metrics
- Loaders: export metrics to target systems
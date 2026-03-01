# jitsu-demo-test
## Project Structure

```
jitsu-demo-ui-test/
├── api/                                # Include class, functions to implement api testing
├── data/                               # Test data, data, constant variables or templates for api
│   └── constants                       # Store constants variables
│   └── templates                       # Store json, xml templates
│   └── variables                       # Store constants variables for this project. Example: Time.is website link
├── pages/                              # Pages with locator and functions to serve UI testing
├── tests/
│   └── ui
│       └── timeis_check.spec.ts        # Test file for UI testing with time.is website
│   └── api
│       └── github_check.spec.ts        # Test file for API testing with Github
├── utils                               # utilities for support testing
├── playwright.config.ts                # Playwright configuration
├── package.json                        # Dependencies & npm scripts
└── .env.example                        # SSL environment config reference
```
## How to run test locally
### To run single test
- Open terminal in visual studio code editor and execute below command
#### Run test by test case name
```
npx playwright test -g "<test_case_name>" --project=<selected_browser>
```
Example:
  - Run UI test case: access timing ui - Hanoi
  ```
  npx playwright test -g "access timing ui - Hanoi" --project=chromium
  ```
#### Run test by test case tag
```
npx playwright test --grep "<tag>" --project=<selected_browser>
```
Example:
  - Run API test case with tag: @seleniumHQ
  ```
  npx playwright test --grep "@seleniumHQ" --project=chromium
  ```
### To run multiple tests

### To run all tests

## How to set up project
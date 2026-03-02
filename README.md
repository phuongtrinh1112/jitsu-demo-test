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
## How to set up project on local machine
### Prequesite
- Install visual studio code IDE
- Install node.js
- Clone this repo to local
### Setting up
- Install playwright by open visual studio code then execute command: `npm init playwright@latest`
### Run test
- Follow below segment [How to run test locally](URL "https://github.com/phuongtrinh1112/jitsu-demo-test/blob/master/README.md#how-to-run-test-locally")
### Open report
- Execute command in terminal of visual studio code then execute command: `npx playwright show-report`

## How to run test locally
- Open terminal in visual studio code editor and execute below command
### To run single test
- To run 1 specific test case
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
  npx playwright test --grep "@seleniumHQ" --project=api
  ```
### To run multiple tests
- To run a list of expected test cases or test cases of a specific test plan
#### Run test by test case tag
```
npx playwright test --grep "<shared_tag>" --project=<selected_browser>
```
Example:
  - Run UI test cases with tag: ui. All test cases that has tag @ui will be executed
  ```
  npx playwright test --grep "@ui" --project=chromium
  ```
  - Run 2 specific UI test cases with different tag
  ```
  npx playwright test --grep "@hanoi | @nhaTrang" --project=chromium
  ```
#### Run test by test file name
- To run test cases belong to a test plan
```
npx playwright test <test_file_name> --project=<selected_browser>
```
Example:
  - Run API test cases in github_check.spec.ts file
  ```
  npx playwright test github_check.spec.ts --project=chromium
  ```
### To run all tests
- To run all test cases in this project
```
npx playwright test
```
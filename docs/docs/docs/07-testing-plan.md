# برنامه آزمون | Test Plan

## Test levels
- **Unit tests:** model validation, membership date rules, payment amount validation, role helpers
- **Integration tests:** login + permissions + create plan + assign plan workflows
- **UI/manual tests:** forms, navigation, Persian RTL display, validation messages, responsive layout
- **Regression tests:** rerun core workflows after changes

## Minimum test cases
| ID | Test | Expected result |
|---|---|---|
| T-01 | Valid user signs in | Dashboard for role opens |
| T-02 | Invalid credentials | Access denied with safe message |
| T-03 | Athlete opens manager page | 403/redirect; no private data exposed |
| T-04 | Athlete tries another athlete's record | Access denied |
| T-05 | Membership end date precedes start date | Validation error |
| T-06 | Negative payment amount | Validation error |
| T-07 | Trainer creates valid plan | Plan is saved |
| T-08 | Plan has no exercise items | Rejected or clearly flagged according to final rule |
| T-09 | Athlete opens assigned plan | Plan details are visible |
| T-10 | Athlete opens unassigned plan | Access denied |
| T-11 | Expired membership | Correct status/report appears |
| T-12 | Required field missing | Form shows actionable validation message |

## Test evidence
For the final submission, keep a brief test report with: test ID, date, tester, environment, steps, expected result, actual result, pass/fail, and screenshot if the instructor permits.

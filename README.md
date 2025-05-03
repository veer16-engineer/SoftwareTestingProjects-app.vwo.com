# SoftwareTestingProjects-app.vwo.com
This project involves manual testing of the VWO (Visual Website Optimizer) platform, a popular A/B testing and conversion rate optimization (CRO) tool. The goal is to ensure the platform's functionality, usability, and performance meet user expectations.

Manual Testing Project for VWO (app.vwo.com)

Comprehensive manual testing documentation for VWO (app.vwo.com) including test plan, test cases, and defect reports

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Folder Structure](#folder-structure)
- [Test Plan](#test-plan)
- [Test Cases](#test-cases)
- [Defect Reporting](#Defect Reporting)
- [Technologies & Tools](#technologies--tools)
- [Contributing](#contributing)
- [Contact](#contact)

  ## 🔍 Project Overview

- **Project Name:** Manual Testing for app.vwo.com  
- **Application URL:** [https://app.vwo.com](https://app.vwo.com)  
- **Type of Testing:** Manual Testing  
- **Tools Used:** Excel / Google Sheets (for test case management), Browser Developer Tools  
- **Testers:** QA Team  
- **Environment:** Web (Chrome, Firefox, Edge)

---


## 1.🗂️ Folder Structure
├── Test_Plan/
│   ├── VWO_Test_Plan.docx/pdf
│   └── Test_Strategy.md
│
├── Test_Cases/
│   ├── 01_Authentication/
│   │   ├── TC01_Login_Valid.md
│   │   ├── TC02_Login_Invalid.md
│   │   └── TC03_Password_Reset.md
│   │
│   ├── 02_AB_Testing/
│   │   ├── TC01_Create_Test.md
│   │   ├── TC02_Variation_Setup.md
│   │   └── TC03_Test_Execution.md
│   │
│   └── 03_Reporting/
│       ├── TC01_Results_Dashboard.md
│       └── TC02_Data_Export.md
│
├── Defect_Reports/
│   ├── Bug_Report_Template.md
│   └── Defects_Logged.xlsx
│
├── Assets/
│   ├── screenshots/
│   └── test_data/
│
└── README.md

## 2.📋 Test Plan

### 1. Objective
To validate the critical functionalities of the app.vwo.com platform through manual testing techniques including functional, UI, usability, and compatibility testing.

### 3. Scope
- Login functionality
- Dashboard and reporting
- Campaign creation and management
- User and team settings
- Navigation and responsiveness

### 4. Features to be Tested
- User authentication (Login/Logout/Forgot Password)
- Campaign (Create, Edit, Delete, Schedule)
- Reporting accuracy
- User management
- Interface responsiveness (web only)

### 5. Features Not to be Tested
- Backend APIs
- Load/Performance Testing
- Email Notification Services (outside integration)

### 6. Assumptions
- Application is stable and deployable to the test environment.
- Test data will be available as required.

### 7. Risks
- Frequent UI changes may affect test cases.
- Limited test environment access may restrict full flow testing.

## 📂 Test Case Repository Structure
test-cases/
├── AUTHENTICATION/
│ ├── TC_AUTH_01_Valid_Login.md
│ ├── TC_AUTH_02_Invalid_Login.md
│ └── TC_AUTH_03_Password_Reset.md
├── AB_TESTING/
│ ├── TC_AB_01_Create_Experiment.md
│ ├── TC_AB_02_Configure_Variations.md
│ └── TC_AB_03_Activate_Test.md
├── REPORTING/
│ ├── TC_REP_01_Results_Dashboard.md
│ └── TC_REP_02_Export_Data.md
└── ASSETS/
├── test-data/
└── screenshots/


## ✨ Test Case 
```markdown
### TC_AB_02_Configure_Variations
**ID:** AB-02  
**Priority:** P1 (High)  
**Type:** Functional  
**Requirement:** VWO-REQ-112  

**Preconditions:**
1. Valid admin credentials
2. New experiment created
3. On "Variations" configuration page

**Test Steps:**
1. Click "Add Variation"
2. Enter variation name: "Blue Button"
3. Upload variation image (test-button-blue.png)
4. Set traffic allocation to 50%
5. Save configuration

**Expected Results:**
✓ Variation appears in experiment dashboard  
✓ Traffic allocation shows 50%  
✓ Preview displays blue button image  

**Test Data:**  
Variation names: ["Blue Button", "Control"]  
Images: [test-button-blue.png, test-button-orange.png]  

**Execution:**
| Attempt | Date       | Result | Tester    | Notes               |
|---------|------------|--------|-----------|---------------------|
| 1       | 2025-05-03 | PASS   | Veer S  | Chrome v118         |
| 2       | 2023-05-03 | PASS   | Virbhadra Smith| Firefox v115  |


🔍 Test Case Coverage

 ![deepseek_mermaid_20250503_2a0170](https://github.com/user-attachments/assets/71fee0d5-9ea5-4a71-abb2-d6a2810e5982)

🚨 Defect Reporting
Severity Levels:

🔴 Critical (Blocking)

🟠 High (Major)

🟡 Medium (Minor)

🔵 Low (Cosmetic)

![deepseek_mermaid_20250503_20711f](https://github.com/user-attachments/assets/1c8669be-52b8-46fe-a1f4-23d9d6b29dad)


Defect Template:

markdown
## DEFECT_002_Dashboard_Load_Failure

**Module:** Reporting  
**Severity:** 🔴 Critical  
**Environment:** Chrome 115, Windows 11  

**Steps:**
1. Login as admin
2. Navigate to Reporting
3. Select date range: 2023-11-01 to 2023-11-15

**Expected:** Dashboard loads within 3s  
**Actual:** Blank screen after 10s  
**Frequency:** 100%  
**Workaround:** Refresh 3-4 times  

**Evidence:**  
![Screenshot](/4_Assets/screenshots/defect_002.png)  
📈 Quality Metrics
Metric	Target	Current
Test Coverage	95%	92%
Pass Rate	90%	88%
Critical Defects	0	2
Defect Density	<0.5	0.7

🛠️ Technologies & Tools
Documentation: MS Word, Excel (or Google Docs/Sheets)

Bug Tracking: JIRA, Bugzilla (optional)

Test Management: TestRail, Zephyr (optional)

🤝 Contributing
Contributions, suggestions, and improvements are welcome!

Fork the repository

Create a new branch (git checkout -b feature-branch)

Commit your changes (git commit -m 'Add new test cases')

Push to the branch (git push origin feature-branch)

Open a Pull Request
📬 Contact
QA Lead: [Virbhadra Swami]
Email: gkw.veer16@gmail.com
Slack: #vwo-qa-channel

# QA Assignment Submission
## Vendor Invoice Management Portal

**Prepared by:** Vyas
**Date:** May 2026

---

## Submission Overview

This submission contains structured QA deliverables for the Vendor Invoice Management Portal assignment. The work covers the full spectrum of QA thinking — from business understanding and risk identification through to detailed test cases, traceability, and realistic bug reporting.

---

## Document Index

| File | Description |
|---|---|
| [01_Project_Analysis_and_QA_Strategy.md](01_Project_Analysis_and_QA_Strategy.md) | Project understanding, assumptions, requirement ambiguities, risk analysis, QA strategy, test scenarios, edge cases, API/DB/security validation thinking, and recommendations |
| [02_Test_Cases.csv](02_Test_Cases.csv) | 51 detailed test cases covering vendor registration, login, invoice submission, approval/rejection, notifications, reports, security, and performance — open in Excel or Google Sheets |
| [03_RTM.csv](03_RTM.csv) | Requirement Traceability Matrix mapping all identified requirements to test scenarios and test case IDs — open in Excel or Google Sheets |
| [04_Sample_Bug_Reports.csv](04_Sample_Bug_Reports.csv) | 3 realistic, detailed bug reports with reproduction steps, impact analysis, root cause hypothesis, and fix suggestions — open in Excel or Google Sheets |

---

## Coverage Summary

| Module | Test Cases | Coverage |
|---|---|---|
| Login & Authentication | TC-LOGIN-001 to TC-LOGIN-008 | Functional + Security + Boundary |
| Vendor Registration | TC-REG-001 to TC-REG-004 | Functional + Negative + Validation |
| Invoice Submission | TC-INV-001 to TC-INV-013 | Functional + Negative + Edge Cases |
| Approval / Rejection Workflow | TC-APPR-001 to TC-APPR-010 | Workflow + Role Access + Concurrency |
| Email Notifications | TC-NOTIF-001 to TC-NOTIF-004 | Integration + Error Handling |
| Monthly Reports | TC-RPT-001 to TC-RPT-004 | Data Accuracy + Access Control |
| Security | TC-SEC-001 to TC-SEC-006 | IDOR + Auth + Injection + File Upload |
| Performance | TC-PERF-001 to TC-PERF-002 | Load + Concurrency + SLA Validation |

**Total: 51 test cases across 8 modules**

---

## Key Highlights of This Submission

- **Requirement ambiguities section** documents 24 specific clarification questions that reflect real pre-testing discovery work
- **Risk matrix** covers business, security, operational, and data risks — all grounded in real-world financial portal scenarios
- **Test data** specified for every test case — exact vendor IDs, PO numbers, invoice amounts, file sizes, and credentials, making cases ready to execute without interpretation
- **Vendor registration coverage** tests the full REQ-001 flow including duplicate email, missing fields, and invalid format scenarios
- **Performance test cases** validate SLAs under concurrent load — 50 AP users for report generation (5s SLA) and 20 simultaneous invoice submissions (3s SLA)
- **Edge cases** include concurrent approval conflicts, session timeout during form fill, duplicate invoice detection, and network interruption during upload
- **Bug reports** cover three high-impact defect categories: duplicate submission, incorrect payment forwarding on rejection, and IDOR (Insecure Direct Object Reference) — all common in financial applications
- **API and DB validation thinking** demonstrates end-to-end QA awareness beyond UI testing
- **RTM** maps every identified requirement to at least one test case, with implied requirements explicitly called out

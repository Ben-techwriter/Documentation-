# Release Notes - ACME ITSM Suite
**Release Version:**3.2.0
**Release Date:**2026-04-01

## New Features

--**Bulk Incident Import**
We've introduced a new bulk import capability that allows adminstrators to create multiple incident records at once using csv file. This feature helps reduce manual effort when onboarding large volume of incidents from external systems.

-**Change Approval Notification Dashboard**
With this release, you can view all pending change approvals in a centralized dashboard, giving approvers greater visibility and faster decision making. 

---

## New Features Requiring Configuration Updates

-**Automated Incident Escalation Rules**
We've added configurable escalation rules that automatically reassign incidents when SLAs are breached. This feature requires activating new workflow rules in Incident Management settings. 

-**Custom Approval Chains for Change Requests**
You can now define multi level approval chains for specific change types. To use this feature, update your approval configuration to include the new approval policy options. 

---

## Improvements

-**Enchanced Incident Submission Performance**
We've improved the speed of incident creation, reducing the average submission time by approximately 30%. 

-**Improved Navigation in Change Management**
The Change Management Interface has been redesigned for easier navigation, allowing users to locate approval and implementation details with fewer clicks. 

---

## API/Web Service Updates

-**Incident API V2 Enchancement**
The Incident Create API now supports bulk requests and returns enhanced validation messages for failed records. 

---

## Bug Fixes

-**Fixed Issue where Incident Forms failed to Load**
Resolved an issue where Incident forms did not load correctly for users with limited roles. Users will now experience consistent form behaviour across roles. 

-**Addressed Email notificaiton failure during Escalation**
A defect that prevented escalation emails from being sent has been fixed, ensuring timely notifications to support team and approvers. 

---

## Known Issues

-**PDF Report Export Delay**
We are aware of an issue where exporting large reports to PDF may take longer than expected. Our team is actively working on a resolution and we expect to include a fix in the next release. 

---

## Deprecation Notice

-**Legacy Approval Workflow**
The legacy approval workflow has been deprecated as of this release and will no longer be supported after version 3.3.0. We recommend transitioning to the new configurable approval chains which offer great flexibility and audit tracking. 

---

## Additional Notes
For upgrade instructions and configuration details, refer to **ACME ITSM Suite Administration Guide**. 

If you experience issues not covered in these release notes, please contact **IT Adminstrator** or consult the **Knowledge Base**.

---


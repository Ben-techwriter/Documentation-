## Troubleshooting ITSM ACME Suite - Incident and Change Management
This troubleshooting guide helps users and administrators identify and resolve common issues related to Incident and Change Management in ACME ITSM Suite, including ticket creation, approvals, and notifications. 

---

## Symptom 1: Incident ticket is not created
Users submit an incident through the ITSM portal, but no ticket number is generated and error message may be displayed. 

#### Cause 1: Incident Management Service is not running
The background service responsible for processing incident submission may be stopped or unresponsive.

#### Solution or Workaround 
1. Log in to the application server.
2. Verify the status of the Incident Management service.
3. Start or restart the service if it is not running.
4. Submit a test incident to confirm that ticket creation works correctly.

#### Cause 2: Mandatory fields are missing or misconfigured
One or more of the required fields in the incident form may be hidden, removed, or incorrectly configured. 

#### Solution or Workaround
1. Navigate to Incident form configuration settings.
2. Verify that all mandatory fields are visible and correctly configured.
3. Restore or correct any missing required fields.
4. Save the configuration and retry incident submission.

--- 

## Symptom 2: Change Request stuck in Pending Approval 
Change Request remain in the **Pending Approval** state, and approvers dont receive notification emails. 

#### Cause 1: Email notification service is unavailable
The email notification servcie required to notify approvers may not be running. 

#### Solution or Workaround 
1. Verify the status of the Email notification service.
2. Restart the service if it is stopped.
3. Send a test notification to confirm email delivery.
4. Re-submit the change request for approval.

#### Cause 2: Approver group is not confirmed correctly 
The Change Request may not be associated with the valid approver group. 

#### Solution or Workaround 
1. Open the Change Request record.
2. Verify that the correct approver group is assigned.
3. Update the approval configuration if required.
4. Save the changes and re-trigger the approval workflow.

---

## Symptom 3: Users do not receive ITSM email notifications 
Users do not receive incident updates, approval requests, or resolution notifications via email. 

#### Cause: Email delivery blocked or filtered
Email sent by ITSM system may be blocked by spam filters or incorrect email configuration.

#### Solution or Workaround 
1. Verify that the user's email address is correct in the ITSM system .
2. Ask users to check their spam or junk folders.
3. Ensure that the ITSM sender address is whitelisted.
4. Test email delivery using a sample notification.

---

## Symptom 4: ITSM Portal performance is slow
Users report slow page load times when accessing incident or change management pages. 

#### Cause: High system load or resource constraints
The application server may be experiencing high CPU or memory usage. 

#### Solution or Workaround 
1. Montior server resource utilization.
2. Restart affected services if necessary.
3. Schedule maintenance during non peak hours.
4. Contact system adminstrators if performance issues persists.

> If the troubleshooting steps in this guide do not resolve your issue, contact the IT Service Desk and provide relevant error messages, timestamps, and affected user details. 

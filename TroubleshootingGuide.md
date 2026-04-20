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


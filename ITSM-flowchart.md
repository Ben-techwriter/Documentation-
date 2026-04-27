```mermaid
flowchart TD
A[User Reports Issue/Request] --> B[Service Desk Receives Ticket]

B-->C{Request Type?}
C-->|Incident| D[Incident Management]
C-->|Service Request| E[Request Fulfillment]
C-->|Change Request| F[Change Management]
C-->|Problem| G[Problem Management]

%% Incident Management
D-->D1[Log & Categorize Incident]
D1-->D2[Prioritize Incident]
D2-->D3[Initial Diagnosis]
D3-->D4{Resolved?}
D4-->|Yes| D5[Resolve & Recover]
D4-->|No| D6[Escalate to Support Team]
D6-->D5
D5-->D7[Incident Closure]

%% Service Request
E-->E1[Validate Request]
E1-->E2[Approve if Required]
E2-->E3[Fulfill Request]
E3-->E4[Request Closure]

%%Change Management
F-->F1[Log Change Request]
F1-->F2[Impact & Risk Assessment]
F2-->F3[Change Approval]
F3-->F4{Approved?}
F4-->|Yes| F5[Implement Change]
F4-->|No| F6[Reject/Rework Change]
F5-->F7[Post Implementation Review]
F7-->F8[Change Closure]

%%Problem Management
G-->G1[Root Cause Analysis]
G1-->G2[Identifying Known Error]
G2-->G3[Create Workaround]
G3-->G4[Permanent Fix via Change]

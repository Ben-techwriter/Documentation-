```mermaid
flowchart LR
P[Recurring Service Incidents]
C1[People]-->P
C2[Process]-->P
C3[Technology]-->P
C4[Tools]-->P
C5[Environment]-->P
C6[Measurement]-->P

%%People
C1a[Insufficient Training]-->C1
C1b[Knowledge Gaps in Support Team]-->C1
C1c[High Staff Turnover]-->C1

%%Process
C2a[Weak Problem Management Process]-->C2
C2b[Poor Escalation Procedures]-->C2
C2c[No Root Cause Documentation]-->C2

%%Technology
C3a[Legacy Systems]-->C3
C3b[Unpatched Software]-->C3
C3c[System Design Flaws]-->C3

%%Tools
C4a[Inadequate Monitoring Tools]-->C4
C4b[Disconnected ITSM Tools]-->C4
C4c[No known error database]-->C4

%%Environment
C5a[High workload during peak hours]-->C5
C5b[Infrastructure Constrains]-->C5
C5c[Network Instability]-->C5

%%Measurement
C6a[No trend analysis]-->C6
C6b[Incomplete incident data]-->C6
C6c[Lack of problem KPIs]-->C6

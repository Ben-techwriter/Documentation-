## Incident Management API Documentation
The Incident Management API by ABCExample allows developers to create, manage, and track incidents. This API provides endpoints for incident creation, incident updation, and incident resolution or closure, making it ideal for applications that require an incident management feature.


## Authorization

To access the Incident Management API, a valid Bearer token is required. Treat this token as a secret and store it securely, using a key management system if possible. Contact your account manager if you need help generating your token.

**Authorization Header Example**:
```http
Authorization: Bearer <YOUR_TOKEN_HERE>
Content-Type: application/json
```

Replace `<YOUR_TOKEN_HERE>` with your actual token. Include this header in each request to authenticate with the API.

---

## Authentication Failure 
If authentication fails, the API returns the following:

```http:
{
"error": "unauthorized",
"message": "invalid or missing token."
}
```

## Methods

| Method | Description                                    |
|--------|------------------------------------------------|
| GET    | Requests one or more resoruces from the server |
| POST   | Creates one or more resources                  |
| PUT    | Updates a resources                            |
| PATCH  | Adds data to an existing resource              |
| DELETE | Deletes or deactivates a resource              |

<details>

<summary>Create Incident</summary>

**Description**: creates a new incident.
**Endpoint**: `POST/incident`
**Request Body**

 **Request**
```
POST/incidents
Authorization: Bearer <YOUR_TOKEN_HERE>
Content-Type: application/json
{
"title": "Email server outage",
"description": "Users cannot send or receive emails",
"priority": "high",
}
```
**Path Parameter**

| Parameter | Type        | Description                 |
|-----------|-------------|--------------------------   |
|Title      | string      | The name of the incident    |
|Description| string        | Description of the incident |
 |Priority  | string        | Priority of the incident    |


**Response**
The Response 201 - created is as follows

```
{
"incident id": "INC-101"
"status": "open"
"created at": 2026-03-18T09:15:00Z"
}
```

| Parameter | Type | Description                 |
|-----------|-------------|--------------------------   |
|Incident Id     | string         | The Id of the incident    |
|Status          | yes            | Status of the incident |
|created at      | string         | Created date of the incident    |

</details>
<details><summary>Get Incident Details</summary>

**Description**: Retrieves detailed information about a specific incident.
Endpoint: GET /incident/{event_id}

**Path Parameter**
incident_id (integer, required) - The ID of the incident to retrieve.

**Request**

```
GET/incidents/INC-101
```

**Response**

```
{
"Incident id": "INC-101", 
"Title": "Email server outage",
"Description": "Users cannot send or receive emails"
"priority": "high",
"status": "open"
"assigned to": "John Doe", 
"created at": "  "
"updated at": "  "

}
```

|Parameter   | Type   | Description                    |
|------------|--------|---------------                 |
|Incident Id |String  |The Id of the incident          |
|Title       |string  |The title of the incident       |
|Description |string  |The description of the incident |
|priority    |string  |The priority of the incident    |
|status      |string  |The status of the incident      |
|assigned to |string  |The name of the person assigned |
|created at  |string(date/time)| The creation date of the incident |
|updated at  |string (date/time)| The updation time of the incident |

</details>

<details>
<summary>Escalate Incident</summary>

- Description: Escalates an incident.
- Endpoint: POST /incident/{id}/escalate 
- Request Body:



**Request**

```
{
POST /incidents/INC-101/escalate
Content-Type: application/json
"escalationlevel": "P1";
"reason": "customer impact confirmed; escalating from p2"
}
````


**Response**

```
{
  "id": "INC-101",
  "status": "Escalated",
  "escalationLevel": "P1",
  "previousLevel": "P2 ",
  "reason": "Issue persists beyond initial troubleshooting",
  "escalatedBy": "tech001",
  "escalatedAt": "2026-03-18T10:45:22Z"
}

````
</details>
<details>
<summary>Delete Incident</summary>
- Description: Deletes an incident.
- Endpoint: DELETE /incident. 
- Request Body:



**Request**

```
DELETE /incidents/INC-101

````


**Response**

```
{
  "id": "INC-101",
  "status": "Archived",
  "message": "Incident deleted successfully",
  "deletedBy": "admin001",
  "deletedAt": "2026-03-18T14:22:10Z"

}
````
</details>

<details>
<summary>Resolve Incident</summary>
- Description: Resolves an incident.
- Endpoint: POST /incident/{Id}resolve. 
- Request Body:



**Request**

```
POST /incidents/{INC-101}/resolve
{
"resolutionNotes": "Rebooted mail server and restored services.",
  "resolvedBy": "tech001"
}
````


**Response**

```
{

"id": "INC-101",
  "status": "Resolved",
  "resolutionNotes": "Rebooted mail server and restored services.",
  "resolvedBy": "tech001",
  "resolvedAt": "2026-03-18T15:12:45Z",
  "previousStatus": "In Progress"

}
````

---
</details>

<details>
<summary>Severity Levels</summary>
 
| Level | Name | Description |
|-------|------|-------------|
| `P1` | Critical | Complete outage or major customer impact. Immediate response required. |
| `P2` | High | Significant degradation. Urgent response required. |
| `P3` | Medium | Partial impact or workaround available. |
| `P4` | Low | Minor issue, cosmetic or low-impact. |

</details>

<details>
 
<summary>Status Codes</summary>
 
| Code | Meaning | When it occurs |
|------|---------|----------------|
| `200` | OK | GET or PATCH succeeded |
| `201` | Created | POST successfully created a resource |
| `204` | No Content | DELETE succeeded; no body returned |
| `400` | Bad Request | Validation error or missing required field |
| `401` | Unauthorized | Missing or expired Bearer token |
| `403` | Forbidden | Token lacks permission for this action |
| `404` | Not Found | Resource ID does not exist |
| `409` | Conflict | State transition not allowed (e.g. re-opening a closed incident) |
| `429` | Too Many Requests | Rate limit exceeded |
| `500` | Internal Server Error | Unexpected server error; retry with backoff |

</details>

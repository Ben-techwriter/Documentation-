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

## Create Incident

**Description**: creates a new incident.
**Endpoint**: `POST/incident`
**Request Body**
  * title (string, required) - Name of the incident.
  * desciption (string, required) - Description of the incident.
  * priority (string, required) - priority of the incident.



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

**Response**
The Response 201 - created is as follows

```
{
"incident id": "INC-101"
"status": "open"
"created at": 2026-03-18T09:15:00Z"
}
```
## Get Incident Details
**Description**: Retrieves detailed information about a specific incident.
Endpoint: GET /incident/{event_id}
Path Parameter:
incident_id (integer, required) - The ID of the incident to retrieve.

**Request**

```
{
GET/incidents/INC-101
}
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

## Create Incident
- Description: Creates a new incident.
- Endpoint: POST /incident/{id}. 
- Request Body:



**Request**

```
{


}
````


**Response**

```
{


}
````


## Delete Incident
- Description: Deletes an incident.
- Endpoint: DELETE /incident. 
- Request Body:



**Request**

```
{


}
````


**Response**

```
{


}
````

## Resolve Incident
- Description: Resolves an incident.
- Endpoint: POST /incident/{Id}resolve. 
- Request Body:



**Request**

```
{


}
````


**Response**

```
{


}
````




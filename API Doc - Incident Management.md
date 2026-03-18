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

Overview: The create incident API is used to create a new incident. We can use the POST method to create a new incident by specifying the required parameters. The response will ideally be a 201 with newly created incident details. 

**Request**
```
POST/incidents
{
"title": "Email server outage",
"description": "Users cannot send or receive emails",
"priority": "high",
}
```
**

**Response**
The Response 201 - created is as follows

```
{
"incident id": "INC-101"
"status": "open"
"created at": 2026-03-18T09:15:00Z"
}
```



```


```mermaid
flowchart TD
A[Client Application]-->|API Request| B[API Gateway]
B-->C{Authentication Valid?}
C-->|No| D[Return 401 Unauthorized]
C-->|Yes| E[Route Request]
E-->F{Request Type?}
F-->|GET| G[Read Data]
F-->|POST| H[Create Resource]
F-->|PUT/PATCH| I[Update Resource]
F-->|DELETE| J[Delete Resource]
G-->K[Business Logic Layer]
H-->K
I-->K
J-->K
K-->L[Database]
L-->K
K-->M[Format Response]
M-->|API Response|A

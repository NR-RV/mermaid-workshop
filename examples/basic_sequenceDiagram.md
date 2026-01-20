# Basic Sequence Diagram Example

Sequence diagrams show how processes or objects interact with each other over time, displaying the order of messages exchanged.

## Simple Sequence Diagram

```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server
    
    User->>Browser: Enter URL
    Browser->>Server: HTTP Request
    Server->>Browser: HTTP Response
    Browser->>User: Display Page
```

## Sequence Diagram with Loops and Conditions

```mermaid
sequenceDiagram
    participant Client
    participant API
    participant Database
    
    Client->>API: Login Request
    API->>Database: Validate Credentials
    
    alt Credentials Valid
        Database->>API: User Data
        API->>Client: Success + Token
    else Credentials Invalid
        Database->>API: Error
        API->>Client: Login Failed
    end
    
    loop Every Request
        Client->>API: API Call with Token
        API->>API: Validate Token
    end
```

## Resources

- [Mermaid Sequence Diagram Documentation](https://mermaid.js.org/syntax/sequenceDiagram.html)

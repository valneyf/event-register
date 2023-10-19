# event-register

```mermaid
---
title: ER Hackathon Registration
---
erDiagram
    USER ||--o{ USERLINK : has
    USER ||--o{ SUBMISSION : has
    USER {
        int    id           PK
        string name
        string email
        string profile_pic
    }
    USERLINK {
        int    id           PK
        int    user         FK
        string url
        string name
    }
    SUBMISSION {
        int    id           PK
        string registrant
        string title
        string details
        int event           FK
    }
    EVENT ||--o{ SUBMISSION : has
    EVENT ||--o{ EVENT : has
    EVENT {
        int    id           PK
        string registrants
        string details
    }

```

## Pages
 - Home/Landing Page
   - List out all events & hackantons participants
 - Login/Resgistration
 - User Profile
 - User Account
 - Participants page
   - Searchable page
 - Registration page
 - CREATE, UPDATE and DELETE pages
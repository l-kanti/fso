```mermaid
sequenceDiagram
    activate Client
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate Server
    Server-->>Client: POSTs, sends response code of 302 redirect, reloading page
    deactivate Server
    Client-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes.html
    activate server
    Server-->>Client: sends file with response code of 200
    deactivate Server
    Client-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Client-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Client-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server-->>Client: Sends all files with response code of 200
    deactivate server

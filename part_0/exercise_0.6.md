```mermaid
sequenceDiagram
    activate Client
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate Server
    Server-->>Client: Takes in request and JSON, Responds with 201 created
    deactivate Server

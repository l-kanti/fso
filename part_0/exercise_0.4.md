```mermaid
sequenceDiagram
    activate Client
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate Server
    Server-->>Client: POSTs, sends response code of 201
    deactivate Server

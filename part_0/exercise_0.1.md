```mermaid
sequenceDiagram
    activate Client
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server-->Client: Sends HTML document file to user
    deactivate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css (due to seeing a reference in html doc)
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js (due to seeing a reference in html doc)
    activate Server
    Server-->>Client: Sends CSS file to user
    Server-->>Client: Sends JS file to user
    deactivate Server
    activate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json (AJAX request)
    deactivate Server
    User pushes button that executes logic to post a new_note, json contains note creation date and note text
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note (done by AJAX)
    activate Server
    Server-->>Client: POSTs, sends response code of 200

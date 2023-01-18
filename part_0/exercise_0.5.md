```mermaid
sequenceDiagram
    activate Client
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.html
    activate Server
    Server-->>Client: Sends html file with response code of 200
    deactivate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate Server
    Server-->>Client: Sends css and js file with response codes of 200
    deactivate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json (performs via js)
    activate Server
    Server-->>Client: Responds with json file
    deactivate Server

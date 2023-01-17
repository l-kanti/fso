```mermaid
graph TD;
sequenceDiagram
    participant browser
    participant server

    browser ->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server -->>browser: HTML document
    deactivate server

    browser->>server: GET https://...
    activate server
    server -->>browser: the css file
    deactivate server

```mermaid
sequenceDiagram
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server-)Client: Sends HTML document file to user
    Client does a request to get the css and js files mentioned in the html file
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server-)Client: Sends CSS file to user
    Server-)Client: Sends JS file to user
    Client does a request to json file by executing the js file
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    User pushes button that executes logic to post a new_note, json contains note creation date and note text
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note

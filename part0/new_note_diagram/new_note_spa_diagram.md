```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>browser: On form submit 
    Note right of browser: Excutes the javascript code it fetched before from the server
    Note right of browser: Prevents default handling of form submit which causes a new GET request
    Note right of browser: Renders the newly added note
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Note right of browser: Content type : application/json
```
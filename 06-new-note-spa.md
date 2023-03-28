```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server
    Note right of browser: The POST request is sent by JS code in the browser, not by form action/ method.
    Note right of browser: Pushes the new note to the note list and rerender the page, all in the front-end.
```

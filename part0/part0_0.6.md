```mermaid 
sequenceDiagram
    participant browser
    participant server

    Note right of browser: The note is added to the page immediately using the DOM-API, before sending it to the server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: Server saves the note
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: The browser stays on the same page doesn't send further requests 
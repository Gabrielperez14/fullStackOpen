```mermaid
sequenceDiagram
    note over Client: When the button on the form is clicked,<br/> the browser will send the user input to the server.
    Client->>+Server:  POST https://studies.cs.helsinki.fi/exampleapp/new_note
   note over Server: The server creates a new note object,<br/> and adds it to an array called notes
    Client->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server-->>-Client: HTML Document
    Client->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server-->>-Client:Css file
    Client->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server-->>-Client: JavaScript file
    note over Client: The browser starts executing the js code<br/> that fetches the Json from the server 
    Client->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server-->>-Client: Json content
    note over Client: Browser renders the new notes
``` 

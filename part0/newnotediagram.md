```mermaid


sequenceDiagram
    title Exercise 0.4 New
    actor user
    participant browser
    participant server
    

    user->>browser: Click on submit button
   
    browser->>server: (POST REQUEST) Send user input to the server
    note right of browser: Data is sent as the body of the POST 

    activate server
    note left of server: The server creates a new note object, and adds it to an array called notes.
    note left of server: Each note object has two fields: content containing, date and time was sent.
    
    note left of server: 302 status code response
                        
    deactivate server

    activate browser
    note right of browser: Reload
    deactivate browser
    browser->>server: (GET REQUEST) fetch main.css
    server->>browser: send main.css
    browser->>server: (GET REQUEST) fetch main.js
    server->>browser: send main.js
    browser->>server: (GET REQUEST) fetch modified data.json
    server->>browser: send data.json with the data previously submitted 
    browser->>user: Render page

   




```mermaid


sequenceDiagram
    title Exercise 0.4 New
    actor user
    participant browser
    participant server
    

    user->>browser: Click on submit button
   
    browser->>server: (POST REQUEST) Send user input to the server
    
    activate server
    note left of server: 302 status code response
    deactivate server

    activate browser
    note right of browser: Reload
    deactivate browser
    browser->>server: (GET REQUEST) fetch main.css
    server->>browser: send main.css
    browser->>server: (GET REQUEST) fetch main.js
    server->>browser: send main.js
    browser->>server: (GET REQUEST) fetch data.json
    server->>browser: send data.json
    browser->>user: Render page

   




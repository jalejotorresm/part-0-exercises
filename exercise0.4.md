New Note Diagram

```mermaid
sequenceDiagram
    participant myUser
    participant theBrowser
    participant theServer

    myUser->>theBrowser: Writes something and saves it
    theBrowser->>theServer: POST /new_note
    Note right of theBrowser: This submits the form with the note content

    theServer->>theBrowser: Forwarding to Main page
    theBrowser->>theServer: GET /
    theServer->>theBrowser: index.html HTML File with the new note added

    theBrowser->>theServer: GET /main.css
    theServer->>theBrowser: main.css CSS File with the page styles

    theBrowser->>theServer: GET /main.js
    theServer->>theBrowser: main.js JavaScript File with the note handling code

    theBrowser->>myUser: Reloaded webpage with the updated note list
```

![./assets/0.4.PNG](./assets/0.4.PNG)

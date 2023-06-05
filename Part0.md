# 0.4 New note diagram
"the user creates a new note on the page https://studies.cs.helsinki.fi/exampleapp/notes by writing something into the text field and clicking the submit button."

title submit form

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/new_notes
server-->browser:302 redirection
note over browser:
browser starts redirection
and then overload /notes
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server-->browser: HTML-code

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
![image](https://github.com/Owen-Lee-io/FullStackDev/assets/47958868/e65d0d3d-f490-4df4-a406-924b5a7c0f4f)


# 0.5: Single page app diagram
"depicting the situation where the user goes to the single-page app version of the notes app at https://studies.cs.helsinki.fi/exampleapp/spa"

title goes to the single-page

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
server-->browser: HTML-code

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->browser: spa.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note

![image](https://github.com/Owen-Lee-io/FullStackDev/assets/47958868/fe41cfa2-c839-4302-adc1-30a54daf93cc)

# 0.6: New note in Single page app diagram
"the user creates a new note using the single-page version of the app."

title creates a new note using the single-page

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa 
browser->server:JSON [{ content: "SAP submit"date: "2023-06-05T12:34:57.194Z", ...]

server-->browser: 201
![image](https://github.com/Owen-Lee-io/FullStackDev/assets/47958868/5810301a-ee51-498a-a61d-fe2a42c16e9a)




 __  __            _            _ ___   
|  \/  |_  _ _ __ | |__  ___ _ | / __|  
| |\/| | || | '  \| '_ \/ _ \ || \__ \  
|_|  |_|\_,_|_|_|_|_.__/\___/\__/|___/  

# Mumbo

Mumbo is an extremely lightweight, simple-to-modify client-server application hosted on your local machine.

When you just need to quickly throw up a GUI application for performing a variety of tasks on your machine, 
this is the fastest, most powerful, most beautiful way known in this corner of the Universe.

## How to Run
A Windows shortcut is included as an example to provide convenient double-click behavior for the application.
The Shortcut is simply running:

```
node main.js
```

The `main.js` script uses bundled dependencies from `mumbo.js` to run the application.  
All the business logic for the application resides in the raw JavaScript code in `main.js`.

> Mumbo assumes a default Google Chrome executable location, but you can easily provide your own directly by editing `main.js`.

## Front End
The front end is served as an HTML5 web application.  
In this implementation it runs using Google Chrome in "app" mode so that the appearance is more like that of a native application.
The entire front end presentation resides in the file `index.html`.

## Server
The server is a NodeJS Express server using the "ws" library to provide websocket connection with the front end client.

### Invoking Local Executables
The server can invoke local executables provided that they are children of the application scripts parent directory.  
This could be easily modified to whitelist a different directory instead.
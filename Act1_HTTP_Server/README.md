# Act1_HTTP_Server
## 👥 Activity Partners
| Role | Name |
| :--- | :--- |
| Lead Coder | [Francis Wayne Preagido] |
| Assistant   | [Robbie Alan Abayan]  |
| Documenter | [Robbie Alan Abayan] |
## 🎯 Objective
This server was built to demonstrate fundamental socket programming in
C, specifically handling simple HTTP GET requests and responding with
200 OK or 400 Bad Request status codes, compiled using MinGW and the
Winsock API.
## 🚀 How to Run the Server (Full Documentation)
### Prerequisites
1. *GCC/MinGW:* Installed and configured in the system PATH
(verified with gcc --version).
2. *Git:* Installed for version control.
3. *Terminal/Command Prompt:* Ready to use.
### Compilation
1. Navigate to the repository folder:
 
 cd Act1_HTTP_Server
 
2. Compile the server.c file. The -lws2_32 flag is crucial for
linking the Winsock library on Windows:
 
 gcc server.c -o http_server.exe -lws2_32
 
### Execution
1. Execute the compiled program:
 
 ./http_server.exe
 
 The console will display: Server listening on port 8080...
### Testing
The server is designed to test two scenarios:
#### A. Test 1: 200 OK (Successful GET Request)
* *Action:* Open a web browser (Chrome, Firefox, etc.) and go to:
 http://127.0.0.1:8080
* *Result:* The server should log the GET request, and the browser
should display the "Success!" HTML body.
#### B. Test 2: 400 Bad Request (Invalid/Unsupported Request)
* *Action:* Use a terminal tool like curl to send an unsupported
method (e.g., POST):
 
 curl -i -X POST [http://127.0.0.1:8080](http://127.0.0.1:8080)
 
* *Result:* The server should log the POST request, and the terminal
should show the HTTP/1.1 400 Bad Request response header.
127.0.0.1
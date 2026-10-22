# EX01 Developing a Simple Webserver
## Date:22/10/2026

## AIM:
To develop a simple webserver to serve html pages and display the Device Specifications of your Laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<!DOCTYPE html>
<html>
<head>
    <title>My Webserver</title>
</head>
<body>
    <h1>Welcome!</h1>
</body>
</html>
"""

class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Request received")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 8000)
httpd = HTTPServer(server_address, MyHandler)
print("My webserver is running...")
httpd.serve_forever()

## OUTPUT:
<img width="261" height="220" alt="Screenshot 2026-10-22 092157" src="https://github.com/user-attachments/assets/f214f868-9c5c-439f-b523-b7b6dc650aba" />
<img width="1413" height="248" alt="Screenshot 2026-10-22 092545" src="https://github.com/user-attachments/assets/d39538a8-cae1-4e26-8ed3-77302c37c048" />

## RESULT:
The program for implementing simple webserver is executed successfully.

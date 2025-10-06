# EX01 Developing a Simple Webserver

# Date:6/10/2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
   <head>
      <title>
          
      </title>
   </head>
<body>
    <h1>DEVICE SPECIFICATION(karthiga sri)</h1>
    <table border="5"cellpadding="10"cellspacing="10";
    <tr bgcolour="yellow">
       <th>S.NO</th>
       <th>DEVICE SPECIFICATION</th>
       <th>TYPE</th>
    </tr>
    <tr>
        <td>1</td> 
        <td>Device name</td>
        <td>TMP215-75-G2</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Processor</td>
        <td>Intel(R) Core(TM) Ultra 5 125H (1.20 GHz)</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Installed RAM</td>
        <TD>16.0 GB(15.5 GB usable)</TD>
    </tr> 
    <tr>
        <td>4</td>
        <td>Device ID</td>
        <td>A0845275-AD9C</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Product ID</td>
        <td>0034-42786-663524</td>
    </tr>
    <tr>
        <td>6</td>
        <td>System type</td>
        <td>64-bit</td>
    </tr>
</body>
</htmL>

"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
# OUTPUT:
![alt text](<Screenshot 2025-10-07 014226.png>)
![alt text](<Screenshot 2025-10-07 013939.png>)
# RESULT:
The program for implementing simple webserver is executed successfully.

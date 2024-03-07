# EX01 Developing a Simple Webserver
## Date:7/3/24

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:

```
Developed by:Swetha D
Register no:212223040222
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
      <title>top 5 software industries</title>
      <body>
             <table border="2" cellspacing="10" cellpaddding="6">
                     <caption> Top 5 Revenue Generating Software Companies </caption>
                     <tr>
<th>s.no</th>
<th>companies</th>
<th>revenue</th> 
</tr>  
<tr> 
<th>1</th>
<th>Microsoft</th>
<th>65 billion</th>
</tr>
<tr>
<th>2</th>
<th>oracle</th>
<th>29.5 billon</th>
</tr>
<tr>
<th>3</th>
<th>IBM </th>
<th>29.1 billon</th>
</tr>
<tr>
<th>4</th>
<th>SAP</th>
<th>6.4 billon</yh>
</tr>
<tr>
<th>5</th>
<th>symentec</th>
<th>5.6 billion</th>
</boby>
</html>
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

```

## OUTPUT:
![Screenshot (4)](https://github.com/swethaDhanraj/simplewebserver/assets/151993685/31f0a910-5ca7-4320-96b7-5ee41cc957dc)

![Screenshot (3)](https://github.com/swethaDhanraj/simplewebserver/assets/151993685/beddf123-2320-4f3a-872c-18077b716f94)

## RESULT:
The program for implementing simple webserver is executed successfully.

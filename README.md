# Developing a Simple Webserver
## Name:Bhuvanesh.S.R
## Ref no:23013380
## Dept:AIML
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.self_response(200)
        self.send_handler('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 80)
httpd = HTTPServer (server_address, HelloHandler)
httpd.serve_forever()
```
# OUTPUT:
![web server SS](https://github.com/Bhuvanesh-Suresh/Web_server/assets/145742661/7c4a530f-6d52-4b94-93e9-f3ec28c13bf2)

# RESULT:

The program is executed succesfully

# EX01 Developing a Simple Webserver

# Date: 19-10-2024
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
```
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body align="center">
    <h1>MY ASUS TUF15 CONFIGURATION</h1>
    <table border="5" cellbadding="100" width="50%" align="center">
        <tr>
            <th>Configuration</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>Processor</td>
            <td>AMD RYZEN 7 7435HS    3.10GHz
            </td>
        </tr>
        <tr>
            <td>Primary Memory</td>
            <td>16 GB RAM</td>
        </tr>
        <tr>
            <td>system type</td>
            <td>64-bit operating system, x64-based processor</td>
        </tr>
        <tr>
            <td>Dedicated Graphic Memory Capacity
            </td>
            <td>4 GB</td>
        </tr>
        <tr>
            <td>SSD Capacity
            </td>
            <td>512 GB</td>
        </tr>
        <tr>
            <td>Primary Memory</td>
            <td>16 GB RAM</td>
        </tr>
        <tr>
            <td>Clock Speed
            </td>
            <td>Upto 4.4 GHz</td>
        </tr>
        <tr>
            <td>Screen Type</td>
            <td>Full HD, IPS, 300nits, Anti-glare, 100% sRGB, 144Hz Refresh Rate, G-SYNC
            </td>
        </tr>
    </table>
</body>
</html>
```
```
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("Your web server is running....") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```





# OUTPUT:
![Screenshot 2024-12-06 214610](https://github.com/user-attachments/assets/62592986-beb1-4cf1-87db-b1bfbfad7961)

![alt text](<Screenshot (13).png>)

# RESULT:
The program for implementing simple webserver is executed successfully.

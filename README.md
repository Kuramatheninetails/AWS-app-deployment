# AWS-app-deployment
Full details 
# code
#!/bin/bash 
# Use this script for your user data (script from top to bottom) 
# Install httpd (Linux 2 version) 
yum update -y 
yum install -y httpd # This line was missing, it installs httpd 
systemctl start httpd 
systemctl enable httpd 
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html 

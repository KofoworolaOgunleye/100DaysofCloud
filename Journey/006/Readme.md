

# Deploy NodeJS-MySQL App on EC2

## Introduction
This explain how I deployed a simple node js application on Amazon EC2 server and run on a live url.

## Prerequisite
* How to create buckets on S3
* How to create EC2 instance
* How to create RDS Database
* SQL Workbench (optional)


## Use Case

* create an RDS db, make sure to take note of your username, password, dbname and endpoint.
* create your EC2 instances ath secuirty group that has a custom IP of port 3000-4000
* Download these [files](https://drive.google.com/drive/folders/17TyHpgR2UL7Hr2Bd8rmE2UITLn9NBL9a) and edit with visual studio or notepad. 
* opern src folder, App.js file, line 27 http://localhost:3001'- put your ec2 ipv4 ip addr where localhost is.
* Open Nodejs folder- server.js, lines 12-16, input your RDS dbhost endpoint, db username and password and db name
* create an S3 bucket and upload the all the files 
* SSH into EC2, I used Session manager because I added a role while creating the EC2 instance
* Follow these [steps](https://drive.google.com/file/d/14-CPco3svQBvwk6C5PVTxubwFYOIliAO/view?usp=sharing)
* On your browser, http//EC2-address:3000 and fill the form, you shd get a form recieved
* go to your SQL workbench to confirm that the data was successfully added to the db

## Cloud Research
* The Github repo: https://github.com/haresrv/sqldeploy
* https://www.youtube.com/watch?v=3sd1H7kJ-j4  
* https://drive.google.com/drive/folders/17TyHpgR2UL7Hr2Bd8rmE2UITLn9NBL9a


## ☁️ Cloud Outcome

* When editing the App. js file, ensure the url is like this: 'http://3.10.57.60:3001:3001' not 'http://3.10.57.60:3001/:3001' , this took me a looong time to figure out because i copied the ip directly from my browser
* The app is running as soon as you open the terminal and it will terminate as you will close the terminal
* install PM2 (Production manager 2) to keep live the app after closing our terminal or disconnect from remote server

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)

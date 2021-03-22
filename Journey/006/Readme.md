

# Deploy NodeJS-MySQL App on EC2

## Introduction
This explain how I deployed a simple node js application on Amazon EC2 server and run on a live url.

## Prerequisite
* How to create buckets on S3
* How to create EC2 instance
* How to create RDS Database
* SQL Workbench (optional)


## Use Case

* create an RDS db, make sure to take note of your username, password, dbname(cloud337) and endpoint.
* create EC2 instances with security group that has a custom IP of port 3000-4000
* Download these [files](https://drive.google.com/drive/folders/17TyHpgR2UL7Hr2Bd8rmE2UITLn9NBL9a) and edit with visual studio or notepad. 
* opern src folder, App.js file, line 27 http://localhost:3001'- put your ec2 ipv4 ip addr where localhost is.
* Open Nodejs folder- server.js, lines 12-16, input your RDS dbhost endpoint, db username and password and db name
* create an S3 bucket and upload the all the files 
* SSH into EC2, I used Session manager because I added a role while creating the EC2 instance
* Follow these [steps](https://drive.google.com/file/d/14-CPco3svQBvwk6C5PVTxubwFYOIliAO/view?usp=sharing)
* On your browser, http://EC2-address:3000 and fill the form, you should get a "form recieved" response
* Go to your SQL workbench to confirm that the data was successfully added to the database

## Cloud Research
* The Github repo: https://github.com/haresrv/sqldeploy
* https://www.youtube.com/watch?v=3sd1H7kJ-j4  
* https://drive.google.com/drive/folders/17TyHpgR2UL7Hr2Bd8rmE2UITLn9NBL9a


## ☁️ Cloud Outcome

* When editing the App.js file, ensure the url is like this: 'http://3.10.57.60:3001:3001' not 'http://3.10.57.60:3001/:3001' , this took me a looong time to figure out because I copied the IP directly from my browser
* I noticed that the app only works when the terminal is open after running npm install.
* Solved the previous step by Installing PM2, a production process manager for Node. js applications  allows you to keep applications alive forever, to reload them without downtime and to facilitate common system admin tasks, to keep alive the app after closing our terminal or disconnecting from remote server.
* Install by following these steps; Make sure you're in test folder, then do the following
    npm install -g pm2 (to install pm2)
    cd NodeJS
    pm2 start server.js (to start pm2)
    cd ..
    cd src
    pm2 start --name App.js npm -- start
    pm2 list (to list your runnig apps)
    pm2 stop 0 (to stop app with IP 0)
    pm2 delete all (to delete/completely remove the apps from the list)
 * [How to start Reactjs application with PM2 as a service (Linux & MacOS)]
(https://medium.com/@devesu/how-to-start-reactjs-application-with-pm2-as-a-service-linux-macos-854d5df3fcf1)


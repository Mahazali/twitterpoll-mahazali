# twitterpoll-mahazali
## Steps to Setup the Spring Boot Back end app (polls) <br/>
### 1. cloning the app <br />
git clone https://github.com/Mahazali/twitterpoll-mahazali.git <br />
cd polls
### 2. Create Postgresql database
create database polling_app
### 3. Change Postgresql username and password as per your Postgresql installation
open src/main/resources/application.properties file.<br />
change spring.datasource.username and spring.datasource.password properties as per your postgresql installation
### 4. Run the app
You can run the spring boot app by clicking the run icon <br /> -

The server will start on port 5000.<br/>

### 5. Default Roles

The spring boot app uses role based authorization powered by spring security. To add the default roles in the database, I have added the following sql queries in src/main/resources/data.sql file. Spring boot will automatically execute this script on startup -<br/>

INSERT IGNORE INTO roles(name) VALUES('ROLE_USER');<br/>
INSERT IGNORE INTO roles(name) VALUES('ROLE_ADMIN');<br/>
Any new user who signs up to the app is assigned the ROLE_USER by default.<br/>

## Steps to Setup the React Front end app (polling-app-client)
First go to the polling-app-client folder -<br/>

cd polling-app-client<br/>
Then type the following command to install the dependencies and start the application -<br/>

npm install<br/>  npm start<br/>
The front-end server will start on port 3000



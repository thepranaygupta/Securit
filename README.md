# Securit-secure-logging-system

# snapshots

landing page:
![landing page](https://i.ibb.co/VLWL1gj/image.png)
<br/>
login page:
![login page](https://i.ibb.co/WGGMkQ6/image.png)
home page:
![home page](https://i.ibb.co/YcvRTPd/image.png)
![navigation bars](https://i.ibb.co/2qmm0Ng/image.png)

# environment setup

## Database Building

as mySql is used as database therefore install mySQL for your system (if not installed) and <b> create a password to access your database.</b><br/>
decide a name for your database and a name for table that will contain inside it. <br/>
i.e: database will be `securit` and table `users`.<br/>
to build the database, run this query in mysql CLI-
```
CREATE DATABASE securit;
CREATE TABLE users (
username VARCHAR(45) NOT NULL PRIMARY KEY,
password VARCHAR(45) NOT NULL,
ID VARCHAR(45) NOT NULL,
email VARCHAR(45) NOT NULL,
active TINYINT(1) NOT NULL DEFAULT 0,
name VARCHAR(45) NOT NULL,
OTP INT NULL,
OTP_timestamp INT NULL,
OTP_attempt TINYINT NULL,
password_attempt TINYINT NULL);
```

## dotenv file creation

In this dotenv file all keys and credentials for this web app will be stored.<br/>
first things first, create a file named `.env` at the root of the directory, then fill these data
```
PORT='5510'
JWT_token='<create a token>'*
DB_HOST='<hostname>'**
DB_USER='root'
DB_PASS='<enter mysql password>'
DB_NAME='securit'***
MAIL_HOST='<smtp.example.com>'****
MAIL_USER='<no-reply@example.com>'*****
MAIL_PASS='<enter email app password>'******
```

 *create a strong key for <b>JSON Web Token</b>. e.g "se8r5g4t5GB5DF4BgdHd8g7er56wA5D65W6465SA4F654" <br/>
 **type hostname, for local host type 127.0.0.1 <br/>
 ***enter database's name which has been created. as we decided our database name is securit <br/>
 ****enter email host name of which service you're using to send email to users. e.g if you're using your gmail account for this then type 'smtp.gmail.com' <br/>
 *****enter email ID from where email will be sent <br/>
 ******enter app password for email server. <br/>
<i><b><b>Tip:</b> to use gmail as sender generate app password.<br/>
go to the link account.google.com, then go to the security section.<br/>
enable 2-step verification feature. an 'App password' feature will be visible just behind 2-step verification option.<br/>
generate a key by selecting app: mail and your device </b></i> <br/>

## NPM package installation

Install <b>Node JS</b> to run this program in server side.
open a terminal and go to it's root directory. <br/>
type `npm install` to install all NPM libraries mentioned in package.json as dependencies

## Run this app

environment setup is completed.<br/>
now start the server by running `npm start`<br/>
go to the browser and type URL `localhost:5510`<br/>

<br/>
<br/>
<br/>

<b>for any kind of problem or queries contact me </b>

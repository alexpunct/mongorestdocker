Пожалуйста, отправьте POST-запрос с телом

{ 
   "name": "JSX",
   "type": "declarative"
}

на адрес

http://78.155.206.184:3000/api/templates?apiKey=ifna212ASFisfsjaAFFF


curl -SLO 'https://raw.githubusercontent.com/GossJS/mongorestdocker/master/docker-compose.yml'



# Description
Node.js and Express.js REST API with MongoDB services Docker compose file. You can use this for launching a REST api on your server very quickly. 
It will create a MongoDB database with admin and database users and a REST service that will allow you to get and send data from Mongo. It will expose 2 ports, one for connecting directly to Mongo and one for the API. 
The configuration is done through Environment variables which you can add in a `.env` file in this folder since it's already present in .gitignore so it won't be committed if you push this code to your fork. 
You can view a step-by-step tutorial with how this file was created on my [Blog](http://blog.bejanalex.com/2017/03/mongodb-rest-api-interface-in-docker/)

# Requirements

[Docker](https://www.docker.com/community-edition#/download) and [Docker compose](https://docs.docker.com/compose/overview/) are required to run these services.

# Running the services

### Environment variables

Either export each environment variable in the terminal session or add an `.env` file in this folder after cloning it. The following environment variables are available:

- MONGODB_EXPOSED_PORT (the MongoDB port you will expose to the outside world)
- MONGODB_ADMIN_USER (MongoDB admin user)
- MONGODB_ADMIN_PASS (MongoDB admin password)
- MONGODB_APPLICATION_DATABASE (MongoDB database for the REST Api Node.js application)
- MONGODB_APPLICATION_USER (MongoDB REST Api database user)
- MONGODB_APPLICATION_PASS (MongoDB REST Api database password)
- REST_API_EXPOSED_PORT (REST Api port)
- REST_API_APIKEY (REST Api Key that you will need to include as a URL parameter when making HTTP requests)

Here is an example of my `.env` file I used for the Blog example. 

```
MONGODB_EXPOSED_PORT=27017
MONGODB_ADMIN_USER=admin
MONGODB_ADMIN_PASS=adminP4ss
MONGODB_APPLICATION_DATABASE=appdb
MONGODB_APPLICATION_USER=appuser
MONGODB_APPLICATION_PASS=appP4ss
REST_API_EXPOSED_PORT=3000
REST_API_APIKEY=ifna212ASFisfsjaAFFF
```

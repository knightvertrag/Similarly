# Similarly

### A simple flask api for users to check similarity between two pieces of text using spacy, an NLP library.

### Build the project:

The project uses docker for containerization. So you need to have docker-ce and docker-compose on your linux system in order to build the project. You will also need to have mongoDB installed locally for the database to run.

#### Installing Docker CE:

https://docs.docker.com/engine/install/

#### Installing Docker Compose

https://docs.docker.com/compose/install/

#### Installing mongoDB

https://docs.mongodb.com/manual/administration/install-on-linux/

Once you are done installing the docker and compose open up a terminal in the project root and run the following command(you may have to use sudo):

```
docker-compose build
```

This will build the web and database services.

Once the build finishes executing, create and start the containers using the following command:

```
docker-compose up
```

This will start up the development server at localhost:5000.

There is no frontend as of now to input data so you will have to use Postman to send data to the api.

The routes are as follows:

1. `POST localhost:5000/register` Register a user
1. `POST localhost:5000/refill` Refill user tokens
1. `POST localhost:5000/detect` Check the similarity ratio between two pieces of text

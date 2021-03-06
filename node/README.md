## Installation

### Dependencies

The first command required for the installation is:

~~$ npm install~~

or 

    $ yarn

Use yarn instead npm in order to get the correct package version. With some new version of typescript and aws-sdk it will not work. It will be solved asap.

Although, for the environment to work properly, some packages have to be installed globally, so you have to execute these commands next:

    $ npm install -g mocha

    $ npm install -g ts-node

    $ npm install -g typescript

    $ npm install -g nodemon

or

    $ yarn global add mocha

    $ yarn global add ts-node

    $ yarn global add typescript

    $ yarn global add nodemon

Finally, we need to link oasp4fn into our project:
For this, your must clone the project in other folder

    $ mkdir C:\data-collector
    $ cd C:\data-collector
    $ git clone https://github.com/devonfw/serverless-data-collector.git .

Then, you must creat a link:

    $ npm link

And finally, you must link oasp4fn in this project

    $ cd C:\my-thai-star\node\
    $ npm link oasp4fn

## Database

First of all, download DynamoDB in order to work with it in local: [http://docs.aws.amazon.com/...](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)

### Running DynamoDB Local:

    $ java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar

### Create tables:

Delete all tables:

    $ npm run database-delete

Create all tables:

    $ npm run database-create

Insert all data:

    $ npm run database-seeds

To delete+create+insert data:

    $ npm run database

## Execution

### Build

To compile all typescript sources you should run:

    $ npm run build

or 

    $ yarn build

### Start

To switch on the server and send some http petitions on your localhost (http://localhost:8080), run the command:

    $ npm run start

or

    $ yarn start

### Testing

In order to run all unit test, run the command:

    $ npm run test

or

    $ yarn test

It uses a new dynamodb connection and migrate & seed all tables. Then it starts a server at port 9080 and then it run all unit test.

### Debugging

Not implemented yet.

### Nodemon

Build and monitors the server, with the nodemon command instead of node:

    $ npm run serve

or

    $ yarn run serve

After cloning this repository use 
     
     npm install

Create 2 tables( attributes are id and name ) in psql. 1 for producer and another 1 for consumer

          CREATE TABLE name (
          user_id BIGSERIAL PRIMARY KEY,
          name VARCHAR(50) NOT NULL
          );
          
          
        CREATE TABLE consumer (
        user_id BIGSERIAL PRIMARY KEY,
        name VARCHAR(50) NOT NULL
        );

Add your username, database name and password in the consumer.js and producer.js page.

Start your docker locally on PC.

Run the docker command in the vscode terminal

    docker-compose up


Open a command prompt and go to your Kafka folder and run consumer 
     
     .\bin\windows\kafka-console-consumer.bat \ --bootstrap-server localhost:9092,localhost:9093 --topic test-topic \ --from-beginning

Open 2 new terminals in vscode and run producer.js and consumer.js

        node producer.js
        node consumer.js


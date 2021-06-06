# Concurrency Increment Task - Glaucus

## Task

### The task is to consistently increment a number in a database when parallel threads are racing to increment the number.

1. Create a table "Number" in MySQL database with one integer type field.

2. Create a RESTful API using Spring MVC architecture that increments this number.

3. Use Jmeter (Do not use postman because it does not send parallel requests) to call this API with 5000 users so that a lot of parallel requests are sent to server to increment the number.

4. Now set the initial value of "Number" table to 0.

5. After the execution of Jmeter, the value of the number in the database shall be 5000. (Try the same with a bigger number 100000)

6. The API should be scalable i.e. if deployed on multiple machines with same database, the result should be consistent.



## Instructions to run this project-

1. Open you IDE, import project then select MAVEN.
3. Run maven refresh to update all the libraries and to resolve all the missing packages.
4. Before you start running your springBoot application, update the mySQL database "username" and "password" with your personal mySQL database "username" and "password".
    You can find the file in "src/main/resources/application.yml".
5. Once you have update the mySQL credentials. Now open mySQL cli and Create the schema and table as provided in the "database-instructions" file.
    In short, you need to create a user and provide that user all permissions, then create a schema/db with named "increment", then create a table named "number".
6. Once mySQL db creation are completed, now you can Run this project by launching the Springboot application.
7. Once application started successfully, Open JMeter and import the test script i.e. "increment-text.jmx".
    I have also added the apache-jmeter.zip, just extract the zip to use jmeter.
    In case you forgot how to launch jMeter, go to apache jmeter folder , go inside bin folder there you will find jmeter.bat and jmeter.sh, in case you are using Windows OS then just double click "jmeter.bat" and if you are using mac then run "jmeter.sh".
    To import test script in jmeter, click on Open->select "increment-text.jmx" file.
8. Run the test suite.
9. Run the Jmeter test script.
10. Check the count in the database with the select query in the database-instructions file.

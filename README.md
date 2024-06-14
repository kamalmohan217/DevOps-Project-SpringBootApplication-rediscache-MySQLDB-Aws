# DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/ec8c4201-5bb5-42c7-9996-f740eed7371c)
1. Clone source code present in repo https://github.com/kamalmohan217/spring-rediscluster-cache-mysql.git as shown in screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/10bbff8d-19f1-44a5-876e-6b62b2c0a3f0)
2. Now connect to the MySQL database and create database and table as required for the project.
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/c943c9b0-8b3e-4dac-bb43-cdb390da20b3)
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/cdc2b46f-5324-41c1-9161-335b24bec182)
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/0b772992-59af-400e-89fb-b69c264cae1c)
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/01e61729-e239-42ea-9836-382f51eb9164)
3. Do the entry in the file spring-rediscluster-cache-mysql/src/main/resources/application.properties for spring.datasource.url, spring.datasource.username and spring.datasource.password as shown in the screenshot below.
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/d4b841a4-145a-4922-8f52-c14298d60a6b)
4. Do the entry in the file spring-rediscluster-cache-mysql/src/main/java/com/springredis/cache/SpringRedisCacheApplication.java for Redis hostname, Redis Port and Redis primary key.
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/36faceaa-e81a-492d-9c61-975234b816bd)
5. Build the Code using Maven as shown in the screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/3beb582d-7e3d-46ac-aa4a-050e8f27befe)
6. Start the Spring Boot Application as shown in screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/72af560b-bf05-4469-99d7-eafbd0243772)
7. Now use POST method for entry into the table items from POSTMAN as shown in screenshot below.
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/59f579d1-6bad-4797-b34b-3c82c0a9c0b3)
8. Checked from database and found entry is present in the database table as shown in the screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/54a46bf9-49d4-4743-bf84-15371ec41953)
9. Now Access the entry using GET method from POSTMAN and record the time as shown in the screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/944aaa29-ef37-478b-9a92-359ff5c4480d)
This is the first time we are accessing the data So Application will connect to database and provide the result and you can see from screenshot above the time taken 611ms.
10. Finally Access the entry second time using GET method from POSTMAN and record the time as shown in the screenshot below
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/286b231e-4123-40f0-ac7d-77da9369ea7c)
This time when we access the data then SpringBoot Application will connect with Redis cache and provide the data and hence the time taken is relatively less.
<br><br/>
In below screenshot I checked the entry for Redis Cache
![image](https://github.com/kamalmohan217/DevOps-Project-SpringBootApplication-rediscache-MySQLDB-Aws/assets/128888356/de97b283-88b5-40ca-ae10-6bfd24ed1fb6)
<br><br/>
The motive of this project is to show the advantage of implementing Redis Cache with MySQL database in an Application. Whenever we query any data then Application will connect with the Redis Cache and if it doesn't find the data in cache then it will connect with database and get the data. After geting the data from database it will make an entry in the Redis Cache for the same. So that next time if same data will be queried then Application will conect with Redis Cache and get the data rather than connecting with the database and getting the data and hence the latency for the request has been reduced.

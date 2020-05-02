# iiec_rise_docker_project
This is my docker project to host a ghost webapp. I have used MYSQL in the back-end and ghost server in the front-end.
### <h3>About Ghost - </h3>
 Ghost is a free and open source blogging platform written in JavaScript and distributed under the MIT License, designed to simplify the process of online publishing for individual bloggers as well as online publications.
### <h3> Requirement :-  </h3>
* You will require an O.S. to host this webapp (I have used RHEL8).
* yum should be configured.
### <h3>Process :- <h3>
#### <h4>1.Docker Installation :- </h4>
* To install docker , run this command on terminal `yum install docker-ce --nobest`
#### <h4>2.Run the Docker :- <h4>
* To start the docker we will use this command `systemctl start docker`
#### <h4>3.Download the required Images :- </h4>
* command to download mysql version 5.7 image => `docker pull mysql:5.7`
* command to download ghost version 1-alpine image => `docker pull ghost:1-alpine`
#### <h4>4.Now setup the MYSQL server :- </h4>
* To setup MQSQL use `docker run -dit -e MYSQL_ROOT_PASSWORD=# Enter a password # -e MYSQL_USER=# Enter a username # -e MYSQL_PASSWORD=# Enter a password other than root password # -e MYSQL_DATABASE=#Enter a database name # --name # Enter a name # mysql:5.6 `
#### <h5>5.Docker-compose installation and creation docker-compose file :- </h5>
* commands to install docker-compose :- 
1. `curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
2. `chmod +x /usr/local/bin/docker-compose`
* after installation create a folder using `mkdir mycompose` command
* In that folder create your docker-compose file using `vim docker-compose.yml`
![s1](https://user-images.githubusercontent.com/58412342/80857193-c99c2980-8c6d-11ea-8f5c-0052ab9502e3.png)
#### <h4>6.To start the server :- </h4>
* run this command in the folder where docker-compose file has been created `docker-compose up`
![s2](https://user-images.githubusercontent.com/58412342/80857414-9d81a8you 00-8c6f-11ea-9c2e-749d959c2863.png)
![s3](https://user-images.githubusercontent.com/58412342/80857415-a1adc580-8c6f-11ea-8a5f-65158eaadffa.png)
#### <h4>6.To stop the server :- </h4>
* to stop the server run this command in same folder where you have created your compose file `docker-compose down` or ctrl+c .
![s4](https://user-images.githubusercontent.com/58412342/80857445-f0f3f600-8c6f-11ea-8a44-6f3f5df553ba.png)
#### <h4>7. To access the webapp :- </h4>
* Go to you browser and search `http://localhost:2368/` or `http://192.168..x.x:8081
![s5](https://user-images.githubusercontent.com/58412342/80857739-efc3c880-8c71-11ea-8abf-c93cefefca00.jpg)







# docker-flask-mysql
Flask with MySQL running on Docker.
This is one of the solution for [sysadmin-challenge](https://github.com/wuakitv/sysadmin-challenge
).

### Getting Started
You can run Flask on docker with the commands below.
```
git clone git@github.com:wosami/docker-flask-mysql.git
cd docker-flask-mysql
docker-compose up
```

Check if the Flask is running with curl command like
```
curl http://127.0.0.1:5000

```

### Requirements
* Docker Engine 18.09 or later (Dev Environment 18.09.1)
* Docker compose 1.23 or later (Dev Environment 1.23.2)
* Network accessible web server hosting the docker binary.

### Environment
* MySQL: 5.7
* Python: 2.7
* Pip modules
  * Flask: 0.12
  * Flask-MySQL: 1.4.0

## Why I chose this solution?
I chose this solution because

* I don't know well about docker and docker-compose so I wanted to challenge them.
* Docker is the light way to build the devlopment environment on your client PC like MAC. 
If you use Vagrant with Virtuslbox you have to use your PC's resources more.
* For serviceability and easier management, I wanted to separate the containers. So I used docker-compose not only docker.
* "app.py" shouldn't be modified but flask is only accessible from your own computer, not from any other in the network.
So I added host IP address on "app.py" to indicat it with following [flask official document](http://flask.pocoo.org/docs/0.12/quickstart/). 
Although there is another way probably, I had the time limit so I prioritized to give this solution as a workaround. 
* In this solution, you have to modify the "docker-compose.yml" if you need to save the data permanently.


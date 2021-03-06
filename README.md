# Let's GO Fun The World


## What to do
This assignment will help you familiarize with the micro service architecture based on Golang, 
Cobra and Docker along with the service structure, coding conventions and basic workflow. 
In this assignment, you are going to develop two services named **Company** and **Project** which perform 
Create, Read, Update, Delete and List action with a few calculation logic. 
These APIs will be exposed to both HTTP and GRPC client using Google Protocol Buffer.

### System architecture overview
![System Overview](./asset/system-overview.png)

### System database overview
![System Overview](./asset/database-overview.png)
  
### This assignment consists of 4 repositories
1. [Let's Go Docker](https://github.com/dinhtp/lets-go)
2. [Let's Go PbType](https://github.com/dinhtp/lets-go-pbtype)
3. [Company Service](https://github.com/dinhtp/lets-go-company)
4. [Project Service](https://github.com/dinhtp/lets-go-project)


##  Prerequisite
- Preferred OS: Linux based (Ubuntu or Fedora).
- Complete setup environment.
- protoc v3.15.6
- protoc-gen-go v1.26.0
- Docker and docker compose with sudo permission.
- Git and Basic Git flow.


## How to use
### Docker command
In order to speed up the processing of spinning up the services with in the `docker-compose.yml` file, 
a few shell scripts created to quickly get the LAN IP, bring up and down the docker services. 
It is also required to take a look inside those scripts to understand the logic behind each command.

During the first run or everytime your local machine LAN IP is changed, it is required to execute the `./start`
command before bring up the docker services. Usually, this command is executed only once during each active session.

- Run `./start` to populate the LAN IP to docker environment.
- Run `./up` to bring up all the services in the docker compose file.
- Run `./down` to bring down all the services in the docker compose file.

### GO Rest Service
Each Rest service written and built by Golang will carry a domain name defined in the `nginx.conf` file.
With each domain name, it is required to update the `hosts` file so that your local machine forward the request correctly.
For Linux users, the `hosts` file is located at `/etc/hosts`.
For Windows users, the `hosts` file is located at `C:\Windows\System32\drivers\etc\hosts`.

- Update the service domain name in the `hosts` file. For example: `127.0.0.1 api-go-company.local.com`
- To bring up all the services in the docker compose file, run `./up`
- Check if the service is up and running using `docker ps`

> NOTE: Changes in this repository ARE NOT REQUIRED to be committed into Github

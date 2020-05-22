# Shiny server + Auth0 using Docker-Compose
> Deploying a shiny server web application adding an Auth0 authenticating layer with Docker Containers. 

The following article gives a in-depth description of the installation and configuration on a single server: [Adding Authentication to Shiny Server in 4 Simple Steps](https://auth0.com/blog/adding-authentication-to-shiny-server/) This article containerizes this solution, it is advised to first read the original Auth0 article, we are following the same steps, with some shortcuts. 

The solution contains four different (micro)services, three containerised and one auth0 (freemium) service
1. Nginx - as webserver
2. Shiny-auth0 - as communicating service between Auth0 and Shiny-server
3. Shiny-server - running the shiny application
4. Auth0 - Authentication layer

![Visual Overview of the microservices and the flow](Visual%20Overview.png)


# Getting Started
## Prerequisites
- A (free) [Auth0](https://auth0.com/) account 
- Docker and Docker-Compose installed


## Deploy shiny app with docker-compose
### 1. Configure Nginx
 Check the Auth0 article for more information: [Get Nginx Up and Running](https://auth0.com/blog/adding-authentication-to-shiny-server/#Step-2--Get-Nginx-Up-and-Running)

#### Create SSL certificates
Put your SSL-certificates in the SSL folder, or create self-signed certificates for testing or development. 

#### Configure nginx configuration
If not running local, adjust the nginx.conf file by replacing the '127.0.0.1' with your own domain name or ip address.

> Please note that this nginx configuration is not secure and not suitable for production. Adjust your nginx configuration file using the [Mozilla SSL Configuration Generator](https://ssl-config.mozilla.org/)

### 2. Set up auth0 and shiny-auth0
Read the Auth0 article on [Setting up an Auth0 Account for shiny-auth0](https://auth0.com/blog/adding-authentication-to-shiny-server/#Step-3--Setting-up-an-Auth0-Account-for-shiny-auth0) Change the .env file accordingly

### (optional) Deploy your custom app
Put your own custom app in the Shiny-server folder. If you want to add extra R libraries to the container, please just them to the [Rocker/shiny](https://hub.docker.com/r/rocker/shiny/) Dockerfile to build your own image. Modify the docker-compose.yml file to use your freshly build image instead of the rocker/shiny default. 


### 3. Docker-compose up
To deploy the services, we only have to 'docker-compose up'
``` cmd
docker-compose up
```





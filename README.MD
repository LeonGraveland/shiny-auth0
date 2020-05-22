# Shiny server + Auth0 using Docker-Compose
> Deploying a shiny server web application adding an Auth0 authenticating layer with Docker Containers. 

The following article gives a in-depth description of the installation and configuration on a single server: [Adding Authentication to Shiny Server in 4 Simple Steps](https://auth0.com/blog/adding-authentication-to-shiny-server/) This article containerizes this solution. 

The solution contains four different (micro)services, three containerised and one auth0 (freemium) service
1. Nginx - as webserver
2. Shiny-auth0 - as communicating service between Auth0 and Shiny-server
3. Shiny-server - Running the shiny application
4. Auth0 - Authentication layer

![Visual Overview of the microservices and the flow]('Visual Overview.png')


# Getting Started
## Prerequisites
- A (free) [Auth0](https://auth0.com/) account 
- Docker and Docker-Compose installed


## Deploy shiny app with docker-compose
### 1. Configure Nginx

#### Create SSL certificates
#### Configure nginx configuration
### 2. Set up auth0 and shiny-auth0
https://auth0.com/blog/adding-authentication-to-shiny-server/#Step-3--Setting-up-an-Auth0-Account-for-shiny-auth0

### 3. Docker-compose up

``` cmd
docker-compose up
```





# Shiny server + Auth0 using Docker-Compose
> Deploying a shiny server web application adding an Auth0 authenticating layer with Docker Containers. 

The following article gives a in-depth description of the installation and configuration on a single server: [Adding Authentication to Shiny Server in 4 Simple Steps](https://auth0.com/blog/adding-authentication-to-shiny-server/) This article containerizes this solution. 

The solution contains four different (micro)services, three containerised and one auth0 (freemium) service
1. Nginx
2. Shiny-auth0
3. Shiny-server
4. Auth0


# Getting Started
## Prerequisites
- A (free) [Auth0](https://auth0.com/) account 
- Docker adn Docker-Compose installed


## Deploy shiny app


### 1. Configure Nginx
#### Create SSL certificates
#### Configure nginx configuration
### 2. Set up auth0 and shiny-auth0
https://auth0.com/blog/adding-authentication-to-shiny-server/#Step-3--Setting-up-an-Auth0-Account-for-shiny-auth0

### 3. Docker-compose up

``` cmd
docker-compose up
```





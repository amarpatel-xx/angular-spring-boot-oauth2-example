# angular-spring-boot-oauth2-example
This project contains examples that use angular-auth-oidc-client and Spring Boot with Keycloak and Auth0 backends. There is also role-based authorization.  This example uses the same realm as configured by the open-source project JHipster.  This example can be used to create an Angular application that uses Keycloak (https://www.keycloak.org) or Auth0 (https://www.auth0.com) for authorization and authentication.  The resource-server and resource-server-webflux are example backends which use the Spring Boot non-reactive and reactive/webflux stacks, respectively.  You can augment the Angular and Orchestrator examples with more functionality per your application requirements.  The building blocks for authorization and authentication are already built in.

# Steps to run examples in development environment (using Keycloak):

## Running Keycloak Docker Container:
cd keycloak
docker compose -f keycloak.yml up -d

# Start the Angular Client:
cd oauth2-client
npm i
npm run ng serve

# Start the Non-reactive Spring Boot Backend
cd resource-server
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev

# Start the Reactive Spring Boot Backend
cd resource-server-webflux
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev

# Using a Web-browser, Navigate to:
http://localhost:4200

Click on the Organizations link.  You should see a list of sample organizations.
Click on the Add-ons link.  You should see a list of sample add-ons.

# Acknowledgements
I would like to thank Phase Two (https://github.com/p2-inc/) for inspiration behind this project. 

These examples are made with love by Amar Premsaran Patel (https://github.com/amarpatel-xx/).
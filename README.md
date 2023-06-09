# Get Started


## About Logicea Card Management 
This is a Card Management, querying and fees payment api with Spring Oauth2 JWT authentication and Password encryption using BCrypt Role-based authorization with Spring Security Customized access denied handling Technologies

Spring Boot 3.0 Spring Security JSON Web Tokens (JWT) BCrypt Maven Getting Started
The app has two authentication users for easier testing
1. Normal user (username/password=```logiceaUser/logicea123```)
2. Admin user(username/password=```logiceaAdmin/logicea123```) 

To get started with this project, you will need to have the following installed on your local machine:

## Dependencies
JDK 17+ Maven 3+ To build and run the project, follow these steps:

## Setting up the project
Clone the repository with the command `git clone https://github.com/SebaMutuku/CardManagement.git` for https or ` git clone git@github.com:SebaMutuku/LogiceaCardManagement.git` for ssh
Navigate to the project directory and :
1. Build the project: `mvn clean install -DskipTests` This will build a jar file in target folder
2. If you are running the application as a standalone jar file, be sure to copy `application.yml` into the same location as the jar file and run using command `java -jar jarname.jar &`. & is included to run it on background.
3. If you are running the project using an IDE or from command line use: `mvn spring-boot:run` .
4. The application will be available on http://localhost:9097.
5. If you want to build a dockerfile for your project, ensure you have run `step 1` correctly and works without any issues. You can then build a docker image using the command `docker build -t logicea-card-management .`

## Swagger documentation
Make sure the application is up and access it via link the endpoint `URI/swagger-ui/index.html e.g http://localhost:9097/swagger-ui/index.html`

## Encryption
This is done using library ```jasypt```. Read more about how to do this here https://medium.com/@javatechie/spring-boot-password-encryption-using-jasypt-e92eed7343ab
You also need to add encyption key in your maven environment by running `mvn -Djasypt.encryptor.password=your encryption key`. For now, I have added it to the ```properties.yml```

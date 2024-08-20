# MessagingStompWebsocket
A “Hello, world” application that sends messages back and forth between a browser and a WebSocket server.

## Using WebSocket to build an interactive web application
This guide walks you through the process of creating a “Hello, world” application that sends messages back and forth between a browser and a server. WebSocket is a thin, lightweight layer above TCP. This makes it suitable for using “subprotocols” to embed messages. In this guide, we use STOMP messaging with Spring to create an interactive web application. STOMP is a subprotocol operating on top of the lower-level WebSocket.  
URL : https://github.com/spring-guides/gs-messaging-stomp-websocket

### What You Will Build

You will build a server that accepts a message that carries a user’s name. In response, the server will push a greeting into a queue to which the client is subscribed.

### What You Need

    About 15 minutes

    A favorite text editor or IDE

    Java 17 or later

    Gradle 7.5+ or Maven 3.5+

    You can also import the code straight into your IDE:

        Spring Tool Suite (STS)

        IntelliJ IDEA

        VSCode

### Build an executable JAR

You can run the application from the command line with Maven. You can also build a single executable JAR file that contains all the necessary dependencies, classes, and resources and run that. Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments, and so forth.

You can run the application by using :

    ./mvnw spring-boot:run. 

Alternatively, you can build the JAR file with :

    ./mvnw clean package

and then run the JAR file, as follows:

    java -jar target/gs-messaging-stomp-websocket-0.1.0.jar

Logging output is displayed. The service should be up and running within a few seconds.


### Test the service

Now that the service is running, point your browser at http://localhost:8080 and click the Connect button.

Upon opening a connection, you are asked for your name. Enter your name and click Send. Your name is sent to the server as a JSON message over STOMP. After a one-second simulated delay, the server sends a message back with a “Hello” greeting that is displayed on the page. At this point, you can send another name or you can click the Disconnect button to close the connection.

### Summary

Congratulations! You have just developed a STOMP-based messaging service with Spring.

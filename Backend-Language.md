# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Backend Language

**Context**
The project requires a backend server to host the retail company's information about products and user information such as order history. The language we choose for the server must be able to handle multiple instances of data syncronization and data manipulation in order to create a responsive user experience.

**Decision**
After thorough consideration we have selected Java as the backend language for this project.
- Java has a high performance rating when it comes to server side operations.
- Java supports multithreading and multiple concurrent requests.
- Java is a highly scalable language.
- Java offers a mature ecosystem with large libraries and frameworks.
- Java puts considerable focus towards security.


**Rationale**

- **Performance**:
   - Java has a high performance rating when it comes to backend server operations. This aspect is crusial for a retail app that may experience high traffic. Java's mulitthreaded performance outweighs the performance of Python and high traffic performance of Node.js.

- **Scalability**:
   - As the user base grows, the backend must be able to handle increased traffic loads. Java's clustering and load balancing tools make it an excellent choice for scalability. Python is also scalable, but requires more development effort and potential trouble shooting. Node.js meets current project requirements for performance but lacks the scalability features of Java.

- **Ecosystem**:
   - Java, Python, and Node.js all offer a rich ecosystem of libraries, documentation and community support. Java is selected due to it's prominance it backend server application.

- **Security**:
   -Java pertains enterprise grade security. The language is strongly typed and pertains robust authentication and authorization frameworks which reduce risk of a security breach and simplifies prject development. Node.js offers middleware security from a third party, which increases project complexity. Python has unsatisfactory security features to provide a secure service to the users.

**Consequences**

- **Memory Usage**
   - Java generally requires more memory allocation than other backend languages. This constraint may pose an issue with server hardware limitations. We must be aware of any hardware constraints and implement an effective solution.

- **Complexity**: 
   - The Java language is complex and tends to have a longer development time compared to Python or Node.js. This may affect future scalability. We must be aware of any current or future time constraints and plan development accordingly. 
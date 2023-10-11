# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Data Storage

**Context**
The project requirements state that the user should be able to view products and their purchase history when the application has limited to no internet connecivity. This requirement necessitates a lightweight data storage solution that can store medium to large amounts of data on the mobile device until the application reestablishes a network connection. The solution should be robust, providing accurate data and integrity during various network conditions.

**Decision**
Based the project requirements, we decided to adopt a combination of PouchDB for mobile devices and CouchDB for servers as our data storage solution.
PouchDB (Client-Side):
- PouchDB is designed to support offline-first applications, which enables offline access to product information and purchase history for the user.
- PouchDB pertains robust data synchronization between a local PouchDB client and a remote CouchDB server. This ensures that data remains consistent between the user's device and the server during network unavailability.
- PouchDB is a document-orientated database that stores data in JSON documents, allowing the ability to store medium to large amounts of data on client side.
- PouchDB is compatible with iOS and Android platforms.
- PouchDB permits the execution of CRUD operations when the application lacks internet connectivity. Users can browse products and access purchase history without interruption.
- PouchDB offers mechanisms for resolving data conflicts that may occur during synchronization, maintaining data accuracy.
- PouchDB is free open-sourse software (FOSS) and free to use without the need of purchasing a license.

CouchDB (Server-Side):
- CouchDB offers a reliable and scalable backend storage solution for future scalability.
- Multi-master replication in CouchDB allows for data consistency across multiple devices and servers.
- CouchDB provides a RESTful API, simplifying integration with various client platforms like our client's mobile app.
- CouchDB is free open-sourse software (FOSS) and free to use without the need of purchasing a license.

**Rationale**

- **Ecosystem**
   - The features of PouchDB and CouchDB provide a more coherent, synergetic data storage solution. SQLite offers local database management but requires a seperate server side database to perform a sync. SQLite requires a custom solution in order to syncronize data effectivley without dataloss. 

- **PouchDB Offline-Firt Design**:
   - One of PouchDB's primary aspects is its support for offline mode with data syncronization. The offline-first design ensures a smooth user experience during limited to no network connectivity, providing the user uninterupted access to product information and their order history. This feature eliminates the need to develop a seperate solution for a robust and consistent data syncronization process, which reduces development time. 

- **PouchDB Cross-Platform Compatibility**:
   - PouchDB is compatible on iOS and Android platforms, which simplifies the development for hybrid apps. This allows us to deliver a consistent and reliable user experience.

- **CouchDB Integrity**:
   - CouchDB's reliability, multi-master replication, and RESTful API provide the necessary backend infrastructure for data integrity and consistency for intermittent connectivity.

- **CouchDB Scalability and Performance**
   - As the company expands, the database must be able to accomidate a growing user base. CouchDB has multiple scalability features such as horizontal scalability, load balancing, replication, and partitaioned databases that allow an efficient change in scale with a minimal impact on server performance. 

- **Cost**
   - PouchDB and CouchDB are free open-source software (FOSS) which reduces expansion and scalability costs as the client does not get charged for 

**Consequences**

- **Server Infastructure**:
   - A large point of consideration was the location of server hosting. In order to gain the high level of control, customization, optimization, compatibility and security with CouchDB, the database server would have to be hosted on-premise, which will increase infastructure costs. We found that the reduction in overall project complexity, reduced development time, database reliability, and specific project requirements, CouchDB and PouchDB become a cost effective solution.

- **Complexity**: 
   - While this approach introduces server management complexity, it ensures that the combination of PouchDB and CouchDB provides a robust data storage and synchronization solution, addressing the project's requirements for offline mode and data integrity and medium to large data storage. Implementing SQLite and a seperate backend database would increase syncronization complexity.






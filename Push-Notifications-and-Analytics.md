# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Push Notifications and Analytics

**Context**
We are tasked with selecting a push notifications and analytics provider for our mobile app project for a retail company. The app requires the ability to send push notifications to users for order updates, new product arrivals, and exclusive offers. Additionally, we need a robust analytics solution to track user behavior, including product views, purchases, and loyalty program interactions. Two potential options, Subscribers and Airship, have been evaluated for these purposes.

**Decision**
After a thorough evaluation of both options, we have decided to select Airship as our push notifications and analytics provider for the retail mobile app project. This decision is based on the following considerations:

**Rationale**

- **Daily Client Analytics**:
   - Comprehensive Analytics: Airship offers comprehensive analytics capabilities that can track user behavior, engagement, and interactions within the app. This will provide us with valuable insights into how users interact with our app, enabling us to make data-driven decisions to improve the app's performance and user experience.

- **Push Notifications**:
   - Airship's Expertise: Airship is a specialized provider in the field of push notifications and has a strong reputation for reliability and real-time delivery of notifications. This aligns well with our need to notify customers about order updates, new product arrivals, and exclusive offers in a timely and dependable manner.

- **Integration and Ease of Use**:
   - SDK Integration: Airship provides easy-to-integrate SDKs (Software Development Kits) for both push notifications and analytics, making it straightforward for our development team to implement these features into the app.

- **Scalability**:
   - Support for Growth: Airship has a reputation for scalability, which is essential for our app as the retail company plans to expand its customer base internationally. Airship can accommodate the increased load and user base as the app's popularity grows.

**Consequences**

By selecting Airship as our push notifications and analytics provider, we anticipate the following consequences:

Reliable and timely delivery of push notifications to keep customers informed and engaged.
Access to detailed analytics data to better understand user behavior and optimize the app's performance.
Ease of integration with our app through provided SDKs.
Support for scalability as the app expands to serve an international customer base.


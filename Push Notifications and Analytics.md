# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Push Notifications and Analytics

**Context**
User behavior tracking, and push notifications are essential for this applications function. We need to choose a service that provides detailed insights and metrics, along with reliable notifications. We will be choosing between Airship, and Subscribers.

**Decision**
Based on our client's needs for this application we will be selecting Subscribers. 
Subscribers features:
- Provides daily client analytics: including abandoned cart tracking, graphs , and charts. All located on one dashboard.
- Push notifications: Including customer recapture, coupon creations, promotion and inventory change announcements.
- Low cost: Clear pricing categories.

**Rationale**

- **Daily Client Analytics**:
   - Rationale: Subscribers offers comprehensive daily client analytics, including abandoned cart tracking, graphs, and charts, all conveniently accessible from a single dashboard. This feature aligns perfectly with the client's goal of gaining deep insights into customer behavior and preferences, which is essential for making data-driven business decisions.

- **Push Notifications**:
   - Rationale: Subscribers provides a robust push notification system that includes customer recapture, coupon creations, promotion announcements, and inventory change notifications. This feature enables the client to engage with customers effectively, recover potential lost sales, and drive user engagement through personalized messaging.

- **Low Cost**:
   - Rationale: Subscribers offers transparent and cost-effective pricing categories. This aligns with the client's need for a budget-friendly solution that provides essential features without breaking the bank. By choosing a solution with clear pricing, the client can manage costs effectively and allocate resources efficiently.

**Consequences**

- **Daily Client Analytics**:
   - Enhanced understanding of customer behavior, improved decision-making, and the ability to identify areas for optimization.

- **Push Notifications**:
   - Increased customer retention, higher sales conversion rates, and improved communication with customers.

- **Low Cost**:
   - Cost savings, predictable expenses, and better financial planning for the client's business.


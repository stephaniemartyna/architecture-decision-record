# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Native, Web, or Hybrid Application

**Context**
The decision of which application type to use in a project heavily influences the architecture of the whole project. The project requirements state that the client needs a mobile application. The team will be deciding between Native and Hybrid application types. We must take careful consideration when deciding on the application architecture to ensure the result will be compatalbe, cost effective, time effective, scalable, and efficient.

**Decision**
The team has decided the application will be hybrid.
- Hybrid applications offer cross-platform development.
- Most hybrid implementations offer offline-mode.
- Hybrid applications are generally cost effective.
- Hybrid applications offer rapid development.

**Rationale**

- **Cross-Platform Development**:
   - A significant advantage of hybrid applications is that we can generally use one codebase for multiple device platforms. This approach can significantly reduce project complexity in comparison to native applications that require a codebase for each platform.

- **Cost**:
   - Hybrid application significantly reduce development and maintenance costs by eliminating any additional supporting infrastructure that would be required for a native application approach.

- **Development Time**:
   - Hybrid applications reduce development time due to the simplicity of maintaining a single codebase. Native applications require one or more codebases to accommodate different device platforms.

**Consequences**

- **Performance Optimizations**
   - Hybrid application frameworks, like React Native, can pertain high performance before platform specific optimizations, but native applications provide the advantage of efficient use of platform specific architecture.

- **Third Party Dependency**: 
   - Hybrid applications may rely on third party frameworks and plugins, which simplify and expedite the development process, but pose an increased risk of security breaches. The team must be aware of any potential security issues of any hybrid frameworks and resolve them effectively.

- **App Store Approval**: 
    - Hybrid applications generally enjoy a faster app store approval rate, but the application may run into certain restrictions and guidelines that are associated with hybrid applications. The team must be aware of and rectify any specific nuances before the launch.
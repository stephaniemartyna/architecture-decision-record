# Architecture Decision Record (ADR)
**Scenerio #1 - Mobile Retail App**
**Stephanie Martyna and Sergei Mochalov**
___
> This project involves developing a mobile app for a retail company, focusing on features like product browsing, purchasing, and a loyalty program. Key requirements include supporting offline mode for customers, integrating push notifications for order updates and offers, and implementing secure payment gateways. Additionally, the app will track user behavior, optimize image handling, and support multiple languages for international expansion.

# Image Handling

**Context**
The app will display product images of varying sizes and resolutions. To ensure optimal performance, we must select an image storage solution and implement techniques such as caching, lazy loading, and compression. We will be choosing between Cloudflare, Fastly, and Akamai.

**Decision**
Based on our client's need for international coverage, we will be selecting Akamai. 
Akamai features:
- Streamline workflows related to visual media optimization, management, and delivery.
- Drastically cut down the resources required for responsive web design, saving time and costs.
- Remove the need for labor-intensive and error-prone manual tasks.
- Enable video playback on mobile devices even with high-latency cellular connections.
- Enhance search engine optimization by reducing byte weight and improving responsiveness.
- Lower both storage and network expenses by transmitting fewer bytes.

**Rationale**

- **Streamline workflows related to visual media optimization, management, and delivery.**:
   - Streamlining these workflows ensures that media assets can be efficiently handled, reducing the complexity of managing various formats, sizes, and resolutions. This simplification leads to improved productivity, faster content updates, and a more seamless user experience.

- **Drastically cut down the resources required for responsive web design, saving time and costs**:
   - Responsive web design requires creating and maintaining versions of a website that adapt to various screen sizes and devices. By reducing the time, cost, and effort involved, organizations can allocate resources more efficiently, accelerate development cycles, and deliver a consistent user experience across different platforms.

- **Remove the need for labor-intensive and error-prone manual tasks**:
   - Manual processes in media handling are not only slow but also prone to errors. Automating these processes not only improves efficiency but also ensures a higher level of accuracy, reducing the risk of mistakes in media optimization and delivery.

- **Enable video playback on mobile devices even with high-latency cellular connections**:
   - Enabling video playback on mobile devices, especially in areas with high-latency cellular connections, enhances the accessibility and engagement of content. This can lead to increased user satisfaction, longer time spent on the platform, and potentially higher conversion rates.

- **Enhance search engine optimization by reducing byte weight and improving responsiveness**:
   - Search engines prioritize websites that load quickly and efficiently. By reducing byte weight and improving responsiveness, a website is more likely to rank higher in search engine results. This can result in increased organic traffic and improved visibility for the website.

- **Lower both storage and network expenses by transmitting fewer bytes**:
   - Transmitting fewer bytes not only reduces data transfer costs but also minimizes the storage requirements for media assets. This is particularly beneficial for businesses and organizations that need to manage large volumes of media content, as it leads to cost savings and more efficient use of resources.

**Consequences**

- **Cost**: 
    - Storing images on a CDN may incur costs depending on the selected CDN provider and the volume of data transferred. These costs should be factored into the app's budget.

- **Complexity**: 
    - Implementing image caching, lazy loading, and compression can add complexity to the app's development. Developers need to carefully manage these techniques to ensure they work as intended and do not introduce new issues.

- **Storage Space**: 
    - Caching images locally on users' devices consumes storage space. Developers must strike a balance between caching enough images to improve performance and managing storage constraints.

- **Maintenance**: 
    - Continuous monitoring and maintenance are required to ensure that the CDN, caching, and compression processes function correctly. Over time, as the app evolves, these processes may need adjustments.

- **Image Quality**: 
    - Aggressive image compression can result in reduced image quality. Striking the right balance between image compression and quality is essential to maintain a visually appealing app.

- **User Experience**: 
    - Efficient image handling contributes to a positive user experience. However, if caching or lazy loading is not implemented correctly, users may encounter issues such as delayed image loading or broken images, leading to frustration.

- **Bandwidth Savings**: 
    - While image compression and lazy loading reduce data usage and improve performance, they may also result in bandwidth savings for users. This can be advantageous, especially in regions with limited data connectivity.

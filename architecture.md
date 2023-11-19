# KARMA-NET Architecture Overview and Flow

KARMA-NET integrates the Beckn Protocol with the Mulearn Karma ecosystem, enabling talent discovery within an open network environment. This comprehensive document provides an in-depth explanation of the system's architecture flow, including frontend details and Beckn Protocol integration.

## Architecture Image

![KARMA-NET Architecture](https://camo.githubusercontent.com/a83fe4902f2bca2f6864e716dcfa420db4f9710dd2a595289d187ee5e93da313/68747470733a2f2f692e696d6775722e636f6d2f7874705a4141622e706e67)


## Architecture Flow

### 1. GUI (Frontend Development)

The Graphical User Interface (GUI), built using React.js, acts as the primary interface for user interaction. It includes various features such as user authentication, navigation menus, data displays, and other functionalities for seamless user experience.

#### Authentication in GUI

Utilizing JSON Web Tokens (JWT), the GUI implements secure user authentication. JWT tokens are generated upon successful user login and stored on the client-side. These tokens are then transmitted with subsequent requests, enabling secure access to system resources while maintaining user session integrity.

### 2. Adapter API / JSON Parser for Beckn Schema

The Adapter API serves a critical role, translating and adapting data between the Beckn Protocol schema and the internal system schema. It acts as a middleware, parsing incoming and outgoing data to ensure compatibility and seamless communication within the system.

### 3. Beckn Protocol Implementation

#### BAP (Beckn Adapter APIs for Mulearn Backend)

- **Client:** Manages client-side interactions, facilitating user engagement.
- **RabbitMQ:** Enables asynchronous messaging for inter-component communication.
- **Redis:** Optimizes data retrieval and storage through efficient caching mechanisms.
- **MongoDB:** Acts as the primary database for system and user-related data storage.
- **Network:** Centralized component managing communication across the network.

#### Registry and Gateway

These components serve as the entry point and registry, enabling discovery and interaction among various services within the network. They facilitate easy access to specific data domains and services within the system.

#### BPP (Beckn Protocol Platform)

- **Network:** Manages network-related functionalities for connectivity and communication.
- **RabbitMQ:** Facilitates messaging and communication within the platform.
- **Redis:** Enables efficient data caching for improved performance.
- **MongoDB:** Stores platform-specific data necessary for comprehensive management.
- **Client:** Supports client-side operations within the platform, enhancing user interactions.

### 4. Webhook Configuration

Webhooks are configured to handle communication events, acting as endpoints that trigger specific actions or events within the system.

### 5. Adapter API - Beckn Schema JSON

This component acts as an interface, allowing the adaptation of Beckn Protocol-specific JSON schemas within the system. It ensures seamless integration of Beckn-specific data structures with the internal system, facilitating smooth communication.

### 6. Database Handler API and MongoDB (Dockerized)

The Database Handler API, along with MongoDB, has been Dockerized, consolidating both components into a single unit for simplified deployment. This Dockerization enables easier management and deployment of MongoDB and its associated API handler within the system.

## Conclusion

The detailed breakdown of the KARMA-NET architecture showcases the integration of Beckn Protocol functionalities with the Mulearn Karma ecosystem. The GUI serves as a user-friendly interface, implementing JWT-based authentication, while various components in the backend handle communication, data storage, and system integration across the Beckn Protocol network.

This documentation provides a clear understanding of the system's flow, frontend authentication, Beckn Protocol integration, and individual component functionalities within the KARMA-NET architecture.
<h1 align="center">
JarvisKit - The Open-Source Generative UI Platform
</h1>

<p align="center">
JarvisKit is a framework for building AI-powered applications, inspired by CopilotKit, with a focus on scalability, simplicity, and ease of use.
</p>

<!-- JarvisKit Components -->
<div align="center">
  <picture>
    <img alt="JarvisKit Components" src="https://github.com/JarvisKit/.github/blob/main/images/jarviskit-components.jpg?raw=true"/>
    </picture>
</div>

## Why JarvisKit over CopilotKit?

We have immense respect for what [CopilotKit](https://github.com/CopilotKit/CopilotKit) has achieved in the AI application development space. CopilotKit provides an excellent foundation for building AI-powered applications with its comprehensive toolkit and developer-friendly approach.

However, during our development journey, we encountered specific architectural challenges that required a fundamentally different approach. Rather than working around these limitations, we decided to build JarvisKit from the ground up to address these core issues:

### 🏗️ **Architectural Differences**

#### 1. **Message Store Architecture**
- **CopilotKit**: Message history is typically stored in the agent's state
- **JarvisKit**: Message Store is separated to the Runtime layer to prevent excessive chat history accumulation in agent state, improving performance and scalability

#### 2. **Real-time Communication**
- **CopilotKit**: Uses Server-Sent Events (SSE) for real-time updates
- **JarvisKit**: Implements WebSocket connections to enable multi-participant chat sessions where customers, sales representatives, and AI agents can participate simultaneously in the same conversation

#### 3. **Agent Runtime & Scalability**
- **CopilotKit**: Traditional request-response model
- **JarvisKit**: [Agent Runtime](https://github.com/Jarvis-Kit/Runtime) uses [Jarvis Langgraph SDK](https://github.com/Jarvis-Kit/Langgraph-SDK) to subscribe to RabbitMQ for initiating chat sessions, enabling seamless horizontal scaling of AI agents

#### 4. **Human-in-the-Loop (HITL) Design**
- **CopilotKit**: Basic HITL capabilities
- **JarvisKit**: Robust HITL implementation using carefully designed tool calls, providing more granular control over human intervention points

#### 5. **Event System**
- **CopilotKit**: Standard event handling
- **JarvisKit**: Custom Event system designed for maximum extensibility, allowing developers to create complex interaction patterns and integrations

#### 6. **Distributed Architecture**
- **CopilotKit**: Monolithic approach
- **JarvisKit**: Microservices architecture with separate Runtime and SDK components for better maintainability and scalability

#### 7. **Design Philosophy**
* **CopilotKit**: Respects and fully utilizes components from existing Agent Frameworks such as LangGraph, CrewAI, AG2, etc., enabling developers to leverage the full potential of these frameworks.
* **JarvisKit**: Seeks to minimally alter the way Agent Frameworks are used—just enough to ensure everything still works—while enabling JarvisKit to optimize the overall experience in its own way.

### 🎯 **Our Solution**

JarvisKit addresses these challenges through:

- **[JarvisKit Runtime](https://github.com/Jarvis-Kit/Runtime)**: A robust runtime environment that handles message persistence, real-time communication, and session management
- **[JarvisKit Langgraph SDK](https://github.com/Jarvis-Kit/Langgraph-SDK)**: A powerful SDK for building scalable AI agents with built-in message queue integration
- **[JarvisKit ReactJS SDK](https://github.com/Jarvis-Kit/ReactJS-SDK)**: A powerful SDK for building Generative UI applications

### 🤝 **Respect for CopilotKit**

We want to emphasize that CopilotKit is an excellent choice for many use cases, particularly for:
- Quick prototyping and development
- Standard AI chat applications
- Projects that don't require complex multi-participant scenarios
- Teams looking for a comprehensive, well-documented solution

JarvisKit was born out of specific needs that required architectural changes at the foundation level. We believe both frameworks serve important roles in the AI application development ecosystem, and we're proud to contribute to the open-source community alongside the CopilotKit team.

---

*Choose the right tool for your specific needs. If you need the architectural flexibility that JarvisKit provides, we're here to help. If CopilotKit meets your requirements, it's a fantastic choice.*

*Please note that JarvisKit is undergoing rapid development. As a result, we are currently providing the full source code of the project instead of pre-built libraries. We apologize for any inconvenience this may cause and greatly appreciate your support and contributions.*

*From the JarvisKit team in Hanoi, with ❤️!*

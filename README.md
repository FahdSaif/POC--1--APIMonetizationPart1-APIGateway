# Kong Gateway (OSS)

Kong is open-source! The core version of Kong, known as the Kong Gateway (OSS), is freely available under the Apache 2.0 license, making it an excellent choice for developers and organizations seeking a lightweight, customizable, and community-supported API gateway.

## Key Features

The Kong Gateway offers a comprehensive suite of features for managing and securing your APIs. Here's a breakdown of the key functionalities:

### API Gateway

*   **Proxying and Routing:** Proxy API requests and route them to appropriate backend services.
*   **Load Balancing:** Distribute traffic across multiple backend services to ensure high availability and performance.
*   **Request Transformation:** Modify incoming requests before forwarding them to backend services, and transform responses before sending them back to clients.

### Authentication

*   **Plugin Support:** Supports various authentication methods through plugins, including:
    *   Key Authentication
    *   JWT (JSON Web Token)
    *   Basic Authentication

### Rate Limiting

*   **Granular Control:** Control API usage per consumer or globally to prevent overloading your services and ensure fair usage.

### Monitoring

*   **Logging and Analytics:** Provides logging and analytics capabilities via plugins that integrate with popular monitoring tools like Prometheus and Datadog.

### Plugin Architecture

*   **Extensibility:** Highly extensible with a powerful plugin system, allowing you to customize and extend Kong's functionality to meet your specific needs.
*   **Included Plugins:** A wide range of plugins are available, covering areas such as:
    *   Caching
    *   Traffic Control
    *   Security

### Performance

*   **High Performance:** Built on NGINX and Lua, ensuring high performance and low latency.
*   **Scalability:** Scales efficiently to handle large workloads and high traffic volumes.

### Community-Driven

*   **Active Community:** Supported by a vibrant and active community, with regular updates, contributions, and ongoing development.


# Kong API Management Tutorials

This repository contains code and resources related to a series of tutorials on managing APIs with Kong. The tutorials cover various aspects of Kong, from basic setup to advanced topics like API key management, rate limiting, and monetization.

## Tutorials

1. **Setting Up Kong on Docker: An Easy Guide**
   
   [![YouTube Video](https://img.youtube.com/vi/Bjg1BCWrW5U/0.jpg)](https://www.youtube.com/watch?v=Bjg1BCWrW5U)

2. **Simplifying API Management: Generating and Testing API Keys**
   
   [![YouTube Video](https://img.youtube.com/vi/iLfzm8b-z3E/0.jpg)](https://www.youtube.com/watch?v=iLfzm8b-z3E)

3. **Managing Multiple API Keys for Testing**
   
   [![YouTube Video](https://img.youtube.com/vi/bA68YOXuN64/0.jpg)](https://www.youtube.com/watch?v=bA68YOXuN64)

4. **Managing Multiple API Keys for Testing (Check if continued...)**
   
   [![YouTube Video](https://img.youtube.com/vi/2dmTmxrx3Oc/0.jpg)](https://www.youtube.com/watch?v=2dmTmxrx3Oc)

5. **Cleaning Up: How to Delete Multiple API Keys**
   
   [![YouTube Video](https://img.youtube.com/vi/OiItvVAw3Lk/0.jpg)](https://www.youtube.com/watch?v=OiItvVAw3Lk)

6. **Implementing Rate Limit Policies on API Keys**
    
   [![YouTube Video](https://img.youtube.com/vi/ixoK80672ZQ/0.jpg)](https://www.youtube.com/watch?v=ixoK80672ZQ)

7. **Debugging lesson - Bash Script Debugging for API Key Management**
    
   [![YouTube Video](https://img.youtube.com/vi/z1vGLt_VY2w/0.jpg)](https://www.youtube.com/watch?v=z1vGLt_VY2w)

8. **Facing Challenges in Automating Cron Scripts for API Key Management**
    
   [![YouTube Video](https://img.youtube.com/vi/7wOKrmS34L8/0.jpg)](https://www.youtube.com/watch?v=7wOKrmS34L8)

9. **Debugging Cron Automation: A Closer Look**  

   [![YouTube Video](https://img.youtube.com/vi/r3o7HuV01E4/0.jpg)](https://www.youtube.com/watch?v=r3o7HuV01E4)
   
9.1. **Monetizing APIs: Setting Up and Routing**  

[![YouTube Video](https://img.youtube.com/vi/O09XHPOWyX0/0.jpg)](https://www.youtube.com/watch?v=O09XHPOWyX0)  


10. **Initial Attempts at Cron Automation on Kong**

[![YouTube Video](https://img.youtube.com/vi/859BHMjAyKU/0.jpg)](https://www.youtube.com/watch?v=859BHMjAyKU)
    
13. **Creating a Simple HTML Interface for APIs**  

    [![YouTube Video](https://img.youtube.com/vi/FnqX7998bAI/0.jpg)](https://www.youtube.com/watch?v=FnqX7998bAI)
    

15. **Casual Check-In: Testing and Updates**
    [![YouTube Video](https://img.youtube.com/vi/QW8U84-ptJ4/0.jpg)](https://www.youtube.com/watch?v=QW8U84-ptJ4)
    

16. **Interactive Frontend for Generating API Keys**
    [![YouTube Video](https://img.youtube.com/vi/qwpmtm4vaeM/0.jpg)](https://www.youtube.com/watch?v=qwpmtm4vaeM)
    


## Deployment with Docker

Kong is most easily deployed using Docker. Follow these steps to get started:

1. **Download Docker Desktop:** Download Docker Desktop for macOS (or your respective operating system) from Docker's official site: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

2. **Installation:** Follow the installation instructions provided by Docker for your operating system.

3. **Verify Installation:** After installation, ensure Docker is running by executing the following command in your terminal:

   ```bash
   docker --version

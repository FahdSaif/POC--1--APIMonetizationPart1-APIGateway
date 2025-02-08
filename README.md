# Kong Gateway (OSS)

Kong is open-source! The core version of Kong, known as the Kong Gateway (OSS), is freely available under the Apache 2.0 license, making it an excellent choice for developers and organizations seeking a lightweight, customizable, and community-supported API gateway.

## Key Features

The Kong Gateway offers a comprehensive suite of features for managing and securing your APIs.  Here's a breakdown of the key functionalities:

### API Gateway

*   **Proxying and Routing:**  Proxy API requests and route them to appropriate backend services.
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
*   **Included Plugins:**  A wide range of plugins are available, covering areas such as:
    *   Caching
    *   Traffic Control
    *   Security

### Performance

*   **High Performance:** Built on NGINX and Lua, ensuring high performance and low latency.
*   **Scalability:** Scales efficiently to handle large workloads and high traffic volumes.

### Community-Driven

*   **Active Community:** Supported by a vibrant and active community, with regular updates, contributions, and ongoing development.




# Kong API Management Tutorials

This repository contains code and resources related to a series of tutorials on managing APIs with Kong.  The tutorials cover various aspects of Kong, from basic setup to advanced topics like API key management, rate limiting, and monetization.


# Kong API Management Tutorials

This repository contains code and resources related to a series of tutorials on managing APIs with Kong. The tutorials cover various aspects of Kong, from basic setup to advanced topics like API key management, rate limiting, and monetization.

## Tutorials

1. **Setting Up Kong on Docker: An Easy Guide**
   [![YouTube Video](https://img.youtube.com/vi/Bjg1BCWrW5U/0.jpg)](https://www.youtube.com/watch?v=Bjg1BCWrW5U)

3. **Simplifying API Management: Generating and Testing API Keys**
   
   [![YouTube Video](https://img.youtube.com/vi/iLfzm8b-z3E/0.jpg)](https://www.youtube.com/watch?v=iLfzm8b-z3E)

5. **Managing Multiple API Keys for Testing**
   
   [![YouTube Video](https://img.youtube.com/vi/bA68YOXuN64/0.jpg)](https://www.youtube.com/watch?v=bA68YOXuN64)

7. **Managing Multiple API Keys for Testing (Check if continued...)**
   
   [![YouTube Video](https://img.youtube.com/vi/2dmTmxrx3Oc/0.jpg)](https://www.youtube.com/watch?v=2dmTmxrx3Oc)

9. **Cleaning Up: How to Delete Multiple API Keys**
    
   [![YouTube Video](https://img.youtube.com/vi/OiItvVAw3Lk/0.jpg)](https://www.youtube.com/watch?v=OiItvVAw3Lk)

11. **Implementing Rate Limit Policies on API Keys**
    
   [![YouTube Video](https://img.youtube.com/vi/ixoK80672ZQ/0.jpg)](https://www.youtube.com/watch?v=ixoK80672ZQ)

13. **Debugging lesson - Bash Script Debugging for API Key Management**
    
   [![YouTube Video](https://img.youtube.com/vi/z1vGLt_VY2w/0.jpg)](https://www.youtube.com/watch?v=z1vGLt_VY2w)

15. **Facing Challenges in Automating Cron Scripts for API Key Management**
    
   [![YouTube Video](https://img.youtube.com/vi/7wOKrmS34L8/0.jpg)](https://www.youtube.com/watch?v=7wOKrmS34L8)

17. **Initial Attempts at Cron Automation on Kong**
    
    [![YouTube Video](https://img.youtube.com/vi/859BHMjAyKU/0.jpg)](https://www.youtube.com/watch?v=859BHMjAyKU)

9.1. **Debugging Cron Automation: A Closer Look**  
[![YouTube Video](https://img.youtube.com/vi/r3o7HuV01E4/0.jpg)](https://www.youtube.com/watch?v=r3o7HuV01E4)


10. **Monetizing APIs: Setting Up and Routing**
    
    [![YouTube Video](https://img.youtube.com/vi/O09XHPOWyX0/0.jpg)](https://www.youtube.com/watch?v=O09XHPOWyX0)

12. **Creating a Simple HTML Interface for APIs**
    
    [![YouTube Video](https://img.youtube.com/vi/FnqX7998bAI/0.jpg)](https://www.youtube.com/watch?v=FnqX7998bAI)

14. **Casual Check-In: Testing and Updates**
    
    [![YouTube Video](https://img.youtube.com/vi/QW8U84-ptJ4/0.jpg)](https://www.youtube.com/watch?v=QW8U84-ptJ4)

16. **Interactive Frontend for Generating API Keys**
    
    [![YouTube Video](https://img.youtube.com/vi/qwpmtm4vaeM/0.jpg)](https://www.youtube.com/watch?v=qwpmtm4vaeM)



  ## Deployment with Docker

Kong is most easily deployed using Docker.  Follow these steps to get started:

1.  **Download Docker Desktop:** Download Docker Desktop for macOS (or your respective operating system) from Docker's official site: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

2.  **Installation:** Follow the installation instructions provided by Docker for your operating system.

3.  **Verify Installation:** After installation, ensure Docker is running by executing the following command in your terminal:

    ```bash
    docker --version
    ```

    This command should display the installed Docker version, confirming a successful installation.  Once Docker is running, you can proceed with deploying Kong.  (Further instructions on deploying Kong with Docker would typically follow here, such as pulling the Kong image and running a container.)



    # Kong API Commands Used

This document provides a collection of curl commands used to interact with the Kong API Gateway. Each command is listed with a brief explanation of its function.

| Command | Explanation |
|---------|-------------|
| `curl -i -X GET http://<kong-gateway>/service-path --header "apikey: your_api_key"` | Sends a GET request to a Kong service with an API key in the header for authentication. |
| `curl -i -X POST http://<kong-gateway>:8001/consumers/{consumer_id}/key-auth --data "key=unique_api_key"` | Creates an API key for a specific consumer in Kong. |
| `curl -i -X POST http://localhost:8001/services --data "name=test-service" --data "url=https://jsonplaceholder.typicode.com"` | Creates a new service in Kong that proxies requests to the specified URL. |
| `curl -i -X POST http://localhost:8001/services/test-service/routes --data "paths[]=/test"` | Adds a route to the test-service in Kong, allowing access via the /test path. |
| `curl -i http://localhost:8000/test/posts` | Sends a GET request to the /test/posts endpoint through Kong. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=key-auth"` | Enables the Key Authentication plugin for the test-service. |
| `curl -i -X POST http://localhost:8001/consumers/ --data "username=test-consumer"` | Creates a new consumer in Kong with the username test-consumer. |
| `curl -i -X POST http://localhost:8001/consumers/test-consumer/key-auth --data "key=my-api-key"` | Assigns an API key to the test-consumer. |
| `curl -i http://localhost:8000/test/posts --header "apikey: my-api-key"` | Sends a GET request with an API key in the header for authentication. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=rate-limiting" --data "config.minute=5"` | Enables rate limiting for the test-service, allowing 5 requests per minute. |
| `curl -i -X POST http://localhost:8001/upstreams --data "name=test-service-upstream"` | Creates an upstream in Kong for load balancing. |
| `curl -i -X POST http://localhost:8001/upstreams/test-service-upstream/targets --data "target=192.168.1.1:80"` | Adds a target to the upstream for load balancing. |
| `curl -i -X POST http://localhost:8001/services --data "name=load-balanced-service" --data "host=test-service-upstream"` | Creates a service that uses the upstream for load balancing. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=request-transformer" --data "config.add.headers=X-Custom-Header:custom_value"` | Enables the Request Transformer plugin to add custom headers to requests. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=proxy-cache" --data "config.strategy=memory"` | Enables the Proxy Cache plugin to cache API responses in memory. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=file-log" --data "config.path=/tmp/kong-logs.txt"` | Enables the File Log plugin to log API requests to a file. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=prometheus"` | Enables the Prometheus plugin to export metrics for monitoring. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=ip-restriction" --data "config.deny=192.168.1.0/24"` | Enables the IP Restriction plugin to block requests from a specific IP range. |
| `curl -i -X POST http://localhost:8001/certificates --data "cert=@/path/to/cert.pem" --data "key=@/path/to/key.pem"` | Adds SSL certificates to Kong for secure communication. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=jwt"` | Enables the JWT plugin for token-based authentication. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=oauth2" --data "config.enable_client_credentials=true"` | Enables the OAuth2 plugin for OAuth2.0 authentication. |
| `curl -i -X POST http://localhost:8001/services --data "name=grpc-service" --data "host=grpc-server-host" --data "protocol=grpc" --data "port=50051"` | Creates a gRPC service in Kong for proxying gRPC traffic. |
| `curl -i -X POST http://localhost:8001/routes --data "service.id=<service-id>" --data "headers.User-Agent[]=Chrome"` | Creates a route that matches requests based on the User-Agent header. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=cors" --data "config.origins=*"` | Enables the CORS plugin to allow cross-origin requests. |
| `curl -i http://localhost:8001/status` | Checks the health status of Kong. |
| `curl -i -X POST http://localhost:8001/services/my-api/plugins --data "name=key-auth"` | Enables API key authentication for the my-api service. |
| `curl -i -X POST http://localhost:8001/consumers/paid-user/key-auth` | Assigns an API key to the paid-user consumer. |
| `curl -i -X POST http://localhost:8001/services/my-api/plugins --data "name=rate-limiting" --data "config.minute=100" --data "config.policy=local"` | Enables rate limiting for the my-api service, allowing 100 requests per minute. |
| `curl -i -X PATCH http://localhost:8001/consumers/premium-user/plugins --data "name=rate-limiting" --data "config.minute=unlimited"` | Updates rate limiting for the premium-user to allow unlimited requests. |
| `curl -i -X POST http://localhost:8001/services/my-api/plugins --data "name=http-log" --data "config.http_endpoint=http://your-billing-system.com/logs"` | Enables HTTP logging for the my-api service to send logs to a billing system. |
| `curl -i -X DELETE http://localhost:8001/consumers/non-paying-user/key-auth` | Deletes the API key for the non-paying-user, revoking their access. |
| `curl -s http://localhost:8001/plugins jq` | Lists all installed and configured plugins in Kong. |
| `curl -s http://localhost:8001/services/YOUR_SERVICE_NAME/plugins jq` | Lists plugins configured for a specific service in Kong. |
| `curl -s http://localhost:8001/consumers/YOUR_CONSUMER_NAME/plugins jq` | Lists plugins configured for a specific consumer in Kong. |
| `curl -s http://localhost:8001/plugins jq '.data[] select(.name=="rate-limiting")'` | Checks if the rate-limiting plugin is installed and active. |
| `curl -i -X POST http://localhost:8001/services/api-monetization/routes --data "paths[]=/api"` | Adds a route to the api-monetization service, allowing access via /api. |
| `curl -i -X POST http://localhost:8001/services/api-monetization/plugins --data "name=key-auth"` | Enables API key authentication for the api-monetization service. |
| `curl -i -X POST http://localhost:8001/consumers/test-user/key-auth` | Assigns an API key to the test-user consumer. |
| `curl -i -X DELETE http://localhost:8001/consumers/test-user/key-auth/{old-key-id}` | Deletes an API key for the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq` | Lists all API keys for the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq '.data length'` | Counts the number of API keys for the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq '.data[] {id, key}'` | Lists all API keys with their IDs and keys for the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq '.data sort_by(.created_at) .[0].id'` | Finds the oldest API key ID for the test-user consumer. |
| `curl -i -X DELETE http://localhost:8001/consumers/test-user/key-auth/1234-5678-9101` | Deletes the API key with the specified ID for the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq '.data[] {id, key, created_at}'` | Lists all API keys with their IDs, keys, and creation timestamps. |
| `curl -i -X POST http://localhost:8001/consumers/test-user/key-auth --data "key=my-fixed-key"` | Assigns a specific API key to the test-user consumer. |
| `curl -s http://localhost:8001/consumers/test-user/key-auth jq '.data[] {id, key}'` | Lists all API keys with their IDs and keys for the test-user consumer. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=rate-limiting" --data "config.minute=5"` | Enables rate limiting for the test-service, allowing 5 requests per minute. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=key-auth"` | Enables API key authentication for the test-service. |
| `curl -i -X POST http://localhost:8001/consumers/test-user/key-auth --data "key=my-secret-key"` | Assigns an API key to the test-user consumer. |
| `curl -i http://localhost:8000/test/posts --header "apikey: my-secret-key"` | Sends a GET request with an API key in the header for authentication. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=rate-limiting" --data "config.minute=5"` | Enables rate limiting for the test-service, allowing 5 requests per minute. |
| `curl -i -X POST http://localhost:8001/services/test-service/plugins --data "name=key-auth"` | Enables API key authentication for the test-service. |
| `curl -i -X POST http://localhost:8001/consumers/test-user/key-auth --data "key=my-secret-key"` | Assigns an API key to the test-user consumer. |
| `curl -i http://localhost:8000/test/posts --header "apikey: my-secret-key"` | Sends a GET request with an API key in the header for authentication. |




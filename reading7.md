# Reading 7
# Web Server Deployment
1. What are some common use cases for NGINX?


NGINX, a powerful web server and reverse proxy, serves various purposes in web infrastructure. It excels in load balancing, efficiently distributing incoming traffic across multiple servers to optimize performance and prevent server overload. As a reverse proxy, it handles requests on behalf of other servers, enhancing security by hiding server details and mitigating DDoS attacks. Additionally, NGINX serves as a caching layer, storing frequently accessed content to reduce server load and accelerate content delivery. Its flexibility extends to serving static content swiftly and efficiently, acting as a robust HTTP and reverse proxy server for numerous websites, applications, and APIs.

2. How does NGINX handle tasks that could slow down the web server?

NGINX employs several mechanisms to handle tasks that might otherwise slow down the web server. Firstly, it uses an event-driven, asynchronous architecture, allowing it to handle numerous connections simultaneously without creating new processes for each connection. This approach optimizes resource utilization and ensures efficient handling of concurrent requests. Additionally, NGINX implements features like caching, which stores frequently accessed content in memory, reducing the need to regenerate content upon every request. It also offers load balancing capabilities to distribute traffic across multiple servers, preventing any single server from becoming overwhelmed. Moreover, NGINX's configuration options, such as rate limiting and connection throttling, enable administrators to manage and control traffic, preventing potential slowdowns or service disruptions.

3. Describe, as if to a non-technical friend how to actually pronounce “NGINX”, and why an org might choose to use it.

saying "NGINX" sounds a bit like "engine-ex." You start with the "engine" part, like the word for a car's motor, and then add an "x" at the end. People often say it quickly, like "EN-jin-eks."

Now, why might a company use NGINX? Well, imagine a really busy road. NGINX helps manage the traffic on a website just like a traffic cop manages cars on a road. It's super good at handling lots of people visiting a website at the same time without making it slow or crashing. So, organizations might choose to use NGINX because it keeps their websites running smoothly even when lots of people are trying to visit them all at once!


## Sources
- https://www.nginx.com/resources/glossary/nginx/
- https://chat.openai.com/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/network-architectures-n10-008/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/networking-devices-n10-008/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/network-connectors-2/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/ethernet-standards-n10-008/


# Reading 2
# Network scanning with NMAP
## Why is it important

Network ports are virtual endpoints used by computers to facilitate communication over a network. They allow different applications and services to connect and exchange data. Ports are numbered, and each number corresponds to a specific type of service or protocol. For instance, HTTP typically uses port 80, while HTTPS uses port 443. Ports enable multiple services to run on a single device by allocating different ports to each service, ensuring that data reaches the correct application or service.

1. What is a port? Describe it with an analogy that would help a family member understand.
   
Imagine your house as a computer, and the doors and windows as network ports. Each door or window serves a specific purpose, like the front door is for friends (like a web browser) to visit, the back door is for deliveries (like email), and the windows might be for passing notes (like chat messages).
2. What does a port scanner send to a port to check the current status?
   
3. When a port scanner sends a request to connect, what are the three possible responses? Describe them.

1. Open: If the port scanner receives a response from the target system, indicating that the port is open, it means that there's an active service listening on that port. This response confirms that communication is possible, and the port scanner can proceed to interact with the service running on that port.

2. Closed: A closed port response means that there's no active service listening on that particular port. The target system sends this response to indicate that there's no application or service running on that port, and attempts to establish a connection will fail.

3. Filtered: This response occurs when a firewall or security mechanism blocks the port scanner's request. The target system doesn't respond to the port scanner's request, indicating that it's actively preventing access to that port. This could be due to security configurations, firewall rules, or network filtering mechanisms in place to restrict access.

- These responses help the port scanner understand the state of each port on the target system, assisting in identifying potential vulnerabilities or services running on the network.

4. What is the difference between TCP and UDP?

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are both transport layer protocols used in computer networks, but they have key differences:

1. Connection-Oriented vs. Connectionless:

TCP is connection-oriented, establishing a connection between the sender and receiver before data transfer. It ensures data reliability by providing error checking, acknowledgment of received data, and retransmission of lost packets if necessary.
UDP is connectionless, meaning it doesn't establish a dedicated connection before sending data. It's faster but offers no guarantees regarding data delivery, reliability, or ordering.
2. Reliability and Ordering:

TCP ensures reliable data delivery. It guarantees that data sent from one end is received correctly at the other end, and in the correct order.
UDP does not guarantee reliability or ordering. It's used when speed and efficiency are more critical than ensuring every packet reaches its destination.
3. Header Size and Overhead:

TCP has a larger header size due to its additional functionalities for ensuring reliability. This can introduce more overhead in the transmission.
UDP has a smaller header size compared to TCP, resulting in less overhead, making it more efficient for certain types of applications like real-time communication or video streaming.
4. Usage:

TCP is commonly used for applications that require high reliability and where data integrity is crucial, such as web browsing, email, file transfer (FTP), etc.
UDP is utilized for applications that can tolerate some data loss and prioritize speed, such as online gaming, streaming media, DNS, VoIP (Voice over Internet Protocol), and real-time video/audio communication.
- In summary, TCP provides reliability and ensures data is delivered in order, while UDP sacrifices these aspects for speed and efficiency. The choice between TCP and UDP depends on the specific requirements of the application and the importance of factors like data integrity and speed.

## List and describe the ports used for the following:

- Telnet: Port 23

Telnet is an older protocol used for remote access to devices. It transmits data in clear text, making it less secure. Port 23 is the default port for Telnet.
- SSH: Port 22

SSH is a secure protocol used for secure remote access, file transfers, and command execution. It provides encrypted communication between devices. Port 22 is the default port for SSH.

- DNS: Port 53

DNS resolves domain names to IP addresses. It uses both UDP and TCP, with Port 53 being the standard port for DNS queries and responses.
- SMTP: Port 25 (unencrypted), Port 465 or 587 (encrypted)

SMTP is used for sending emails. Port 25 is the default port for unencrypted SMTP, while ports 465 and 587 are used for encrypted SMTP (SMTPS and STARTTLS).
- HTTP: Port 80

HTTP is used for transmitting web pages and data on the internet. Port 80 is the default port for unencrypted web browsing.
- HTTPS: Port 443

HTTPS is a secure version of HTTP that uses encryption (SSL/TLS) for secure communication over the internet. Port 443 is the default port for encrypted web browsing.
- RDP: Port 3389

RDP allows remote control and access to a computer desktop. Port 3389 is the default port used for RDP sessions.
- Ping: Ping is not associated with a specific port as it operates on the ICMP protocol. It's used to test connectivity between devices and doesn't use ports like other protocols. Instead, it sends ICMP echo request packets and listens for ICMP echo reply packets.

## Analogy
Imagine a massive library with various sections, each dedicated to a different topic or genre. The library has different entrances, each leading specifically to one of these sections. These entrances represent network ports. Just as each entrance guides you to a specific part of the library, ports on a computer guide data to particular services or applications. For example, one entrance might lead to the history section (like port 80 for HTTP), while another leads to the technology section (port 22 for SSH). Each entrance/port serves as a gateway for information to reach its designated destination within the library or computer system.

## Things i want to know more about
Understanding the information that ports transit.
## Sources
- https://www.varonis.com/blog/port-scanning-techniques
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/common-ports-n10-008/
- https://chat.openai.com/
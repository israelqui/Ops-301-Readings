# Reading 3
## Why is it important to learn thins concept?

CIDR block notation efficiently manages IP addresses, optimizing their allocation and use in networks. Network segmentation enhances security by isolating sections, limiting the impact of potential breaches and enabling tailored security measures for different network areas. Together, they bolster network efficiency and resilience against cyber threats.

## CIDR Block Notation
1. What is CIDR notation? a CIDR block?

CIDR notation is a way of representing a CIDR block, which is simply a range of IP addresses. When you create a network, the aim is to make sure there are enough available IP addresses for your use case, without making the CIDR block too large and wasteful.

2. How many octets are found in an IPv4 address?

 four 8-bit decimal numbers

3. Setting binary aside and using the decimal system, what is the range of numbers found in an octet?

256 possible values. However, since we start counting from 0, the range is from 0 to 255 inclusive, resulting in a total of 256 values.

4. What does the final digit after the “/” represent in an IPv4 address?

The subnet mask or prefix length. This number specifies the number of bits in the IPv4 address that are used for the network portion.



5. How many IP addresses are in the CIDR block 10.0.0.0/24?

In CIDR notation, the "/24" indicates that the first 24 bits of the 32-bit IPv4 address are used for the network portion, leaving 8 bits for host addresses. For an IPv4 address, there are 32 bits in total. When you have a "/24" subnet mask, it means there are 32 - 24 = 8 bits available for host addresses. With 8 bits for hosts, you can have 2^8 = 256 unique combinations of host addresses within that network block. However, remember that in any given subnet, the first and last addresses are reserved. So, out of the 256 combinations, the network ID (10.0.0.0) and the broadcast address (10.0.0.255) cannot be assigned to hosts. Therefore, in the CIDR block 10.0.0.0/24, there are 256 - 2 = 254 usable IP addresses for hosts.

## Network segmentation 

1. In your own words, describe network segmentation.

Network segmentation involves dividing a computer network into smaller, isolated sections or segments to enhance security, efficiency, and management. By categorizing devices and systems into distinct segments based on criteria like functionality, security requirements, or departmental divisions, segmentation helps restrict the scope of potential security breaches. It allows for tighter control over traffic flow, limiting the impact of cyber threats or unauthorized access. Moreover, segmentation facilitates the application of specific security measures tailored to each segment's needs, enabling better monitoring, control, and optimization of network resources and performance.

2. Network segmentation isn’t important as long as the network is using a well 
configured firewall. Do you agree? Why or why not?

While a well-configured firewall is a crucial component of network security, relying solely on it without network segmentation might leave vulnerabilities. Network segmentation offers additional layers of protection by compartmentalizing the network into smaller segments. Even with a firewall, a single breach could potentially compromise the entire network if there's no segmentation in place. Segmentation limits the lateral movement of threats within the network, reducing the impact of a breach and preventing attackers from easily accessing critical resources across the entire network. It provides granular control over access, allowing tailored security measures for different segments based on their specific requirements. Combining a robust firewall with effective network segmentation significantly strengthens overall network security.

3. What is a screened subnet?

A screened subnet, also known as a demilitarized zone (DMZ), is a network architecture setup that adds an additional layer of security to protect an internal network from external threats. It typically involves placing servers, services, or resources that need to be accessed from the internet in an isolated network segment called the DMZ. The DMZ sits between an external untrusted network (like the internet) and an internal trusted network (such as a corporate LAN).

The screened subnet employs multiple security measures, including firewalls and other security devices, to control and monitor traffic entering and leaving the DMZ. It allows limited access to resources in the DMZ from the internet while ensuring that direct access to the internal network is restricted. This setup helps mitigate the risk of external threats by creating a buffer zone where potentially vulnerable services are hosted, reducing the chances of a direct attack on the internal network.

4. Cameras, ID card scanners, locked doors and biometrics are just a few examples of what type of security?

They fall under the category of "physical security." Physical security focuses on measures designed to protect physical assets, people, infrastructure, and resources from unauthorized access, damage, or harm. It encompasses tangible elements such as barriers, locks, surveillance systems (like cameras), access control systems (like ID card scanners and biometrics), and environmental design to safeguard physical spaces, buildings, and the items within them. Physical security measures work to deter, detect, and respond to potential threats and vulnerabilities in the physical realm.

## Analogy
A city with various neighborhoods, each marked by different street signs. The CIDR block notation is like a zip code that broadly identifies the city area. Within this city, the neighborhoods represent network segments. Just as houses in a neighborhood share a common zip code but have distinct street addresses for precise identification, CIDR notation designates a range of IP addresses for a network block. Similarly, network segmentation divides the city into neighborhoods, each with its own characteristics, rules, and community, allowing specific security measures and control tailored to the needs of each neighborhood without affecting others in the city.

## Things I want to know more about
- how CIDR notation (Classless Inter-Domain Routing) works, its significance in IP addressing, subnetting, and how CIDR helps in efficient address allocation.
- Understanding the importance of network segmentation in cybersecurity, its benefits in terms of security, traffic control, and resource optimization. Look into different segmentation strategies, such as VLANs, DMZs, and their implementation.

## Sources
- https://medium.com/@ethicalentrepreneur/cidr-block-notation-explained-in-2-minutes-1010ec0dbc15
- https://www.comptia.org/blog/security-awareness-training-network-segmentation
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/classful-subnetting-n10-008/#google_vignette
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/vlans-and-trunking-n10-008/
- https://chat.openai.com/

# Reading 4
# Routing
## Why this topic matters?

Understanding networking concepts such as different network modes in virtualization, port forwarding, and security implications is vital. It enables secure configurations, like isolating virtual machines to prevent unauthorized access, while also facilitating the hosting of servers accessible within local networks. Port forwarding knowledge ensures specific traffic is directed to intended services or devices. Awareness of security risks associated with these configurations helps in making informed decisions to mitigate potential threats, ensuring functional and secure network setups. Overall, comprehending these concepts empowers effective network management, balancing functionality with robust security measures.

1. Which network mode in VirtualBox can be used to emulate unplugging the Ethernet cable from the network?

In VirtualBox, the network mode that emulates unplugging the Ethernet cable from the network is called "Not Attached." When you select the "Not Attached" mode for a virtual machine's network adapter, it essentially isolates the VM from the physical network. This mode is useful for scenarios where you want the VM to operate independently without any network connectivity. It's akin to unplugging the Ethernet cable from a physical machine, ensuring no network communication occurs through that adapter.

2. Which network mode would be best if you wanted to run a server on a VM that could be fully accessible from your physical local area network?

In the Bridged Adapter mode, the VM's network interface is bridged with a physical network adapter on your host machine. This configuration allows the VM to appear as a separate device on your local network, obtaining an IP address directly from your router or DHCP server. As a result, the VM can communicate and be accessed by other devices on the LAN as if it were a physical machine connected to the same network.

When setting up a server on a VM that needs to be reachable and fully accessible within your local network, using the Bridged Adapter mode enables seamless integration of the virtual server with your LAN infrastructure.

3. What are the three options of promiscuous mode and what does each do?


In VirtualBox, the Promiscuous Mode settings are related to how a network adapter within a virtual machine handles network traffic. There are three options:

1. Deny: This mode is the default setting. In "Deny" mode, the VM's network adapter can only receive packets that are specifically addressed to it. It does not see the network traffic of other machines on the same network segment.

2. Allow All: When set to "Allow All," the VM's network adapter can see all traffic on the network segment it is connected to, regardless of whether the packets are addressed to the VM or not. This mode enables the VM to capture and inspect all network traffic passing through the network segment.

3. Allow Promiscuous: This mode is a more refined version of "Allow All." In "Allow Promiscuous" mode, the VM's network adapter can receive all packets that are specifically addressed to it, similar to "Deny" mode. However, it can also capture packets on the network segment if they are not addressed to the VM but are promiscuously broadcast or multicast packets.

These modes are typically used in scenarios where network monitoring, analysis, or specialized networking configurations are necessary within a virtualized environment. However, using promiscuous mode to capture network traffic that is not intended for the virtual machine might raise privacy and security concerns, so it's important to use these modes with caution and only when necessary.

4. What is Port Forwarding?


Port forwarding is a networking technique used to redirect specific communication requests from one address and port number combination to another. It's commonly employed in network configurations, particularly in routers or firewalls, to allow external devices or networks to access services or applications hosted on devices within a local network.

When a device in a local network wants to provide services (such as a web server, FTP server, or gaming server) that need to be accessible from the internet or an external network, port forwarding facilitates this access by forwarding incoming requests from a specific port on the router's public IP address to a specific port on a device within the local network.

For instance, if you have a web server running on port 80 on a computer in your local network with a private IP address, you can set up port forwarding on your router. This configuration will forward incoming requests on port 80 of your router's public IP address to the private IP address of your web server within the local network. As a result, external users can access the web server by navigating to your public IP address in their web browser.

Port forwarding helps in enabling remote access to services behind a router or firewall and is commonly used for applications like online gaming, remote desktop connections, accessing security cameras, hosting websites, and more.

However, it's important to consider security implications when using port forwarding, as opening specific ports and exposing services to the internet can potentially make the network vulnerable to attacks if not properly configured or if the services have security vulnerabilities.

## Analogy

Imagine your network is like a city with different streets and buildings. Understanding network concepts is like knowing the various routes and paths within the city. You need to know which roads (network modes) lead to specific destinations (servers or services) and how to direct traffic (port forwarding) to reach those places efficiently. Just as understanding the city's layout helps you navigate and reach your desired locations while avoiding potential hazards, comprehending networking concepts enables you to manage your network effectively, ensuring that data reaches its intended destination securely and without unnecessary detours.

## Things I want to know more about:

- Network security measures 
- Remote Service Accessibility 
- Risk Management

# Sources:

- https://www.nakivo.com/blog/virtualbox-network-setting-guide/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/network-topologies-5/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/routing-technologies-n10-008/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/n10-008-dynamic-routing/
- https://www.professormesser.com/network-plus/n10-008/n10-008-video/network-switching-overview-n10-008/
- https://chat.openai.com/ 
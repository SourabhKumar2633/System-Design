

# System-Design
## Storage 
- Storage is the collection of methods and technologies that can capture and hold digital information on media.
- Storage is normally described as the data storage devices that are connected to the computer through input or output operations that includes flash devices, hard disks, SAN, NAS, old tape systems and other different types of medium.
  ### Storage Types
  ![image](https://github.com/SourabhKumar2633/System-Design/assets/146738264/fb651608-421e-45e4-8190-2c9b65935f38)
  - There are a lot of options that are available for storing data. The main purpose is deciding which is the most appropriate for you. All are different on the basis of their need and usage criteria e.g. CD, Punch card, Zip disk, DVD, Blu-ray disc, Flash jump drive, Hard Drive, Floppy diskette, NAS, Tape drive, SSD (Solid State Drive), NAS and Cloud Storage. For example, we are using USB Flash drives for our students data management here at Network Walks Academy.
    
  ### 1. DAS (Directly Attached Storage)
   - This is as simple as it sounds DAS (Directly Attached Storage) device. A simple example of DAS is an external hard drive connected through a Universal Serial Bus (USB) cable. When we discuss about storage

## NETWORKING
 ### LOAD BALANCER
 - Load balancing refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.
 - A load balancer acts as the “traffic cop” sitting in front of your servers and routing client requests across all servers capable of fulfilling those requests in a manner that maximizes speed and capacity utilization and ensures that no one server is overworked, which could degrade performance.
 - If a single server goes down, the load balancer redirects traffic to the remaining online servers. When a new server is added to the server group, the load balancer automatically starts to send requests to it.
 -  A load balancer performs the following functions:
   - Distributes client requests or network load efficiently across multiple servers
   - Ensures high availability and reliability by sending requests only to servers that are online
   - Provides the flexibility to add or subtract servers as demand dictates
![image](https://github.com/SourabhKumar2633/System-Design/assets/146738264/b4b1ce45-84bc-413b-9779-656bf0b27391)

 ### Load Balancing Algorithms
 - Different load balancing algorithms provide different benefits; the choice of load balancing method depends on your needs:
  - *Round Robin* – Requests are distributed across the group of servers sequentially.
  - *Least Connections* – A new request is sent to the server with the fewest current connections to clients. The relative computing capacity of each server is factored into determining which one has the least connections.
  - *Least Time* – Sends requests to the server selected by a formula that combines the
fastest response time and fewest active connections. Exclusive to NGINX Plus.
  - *Hash* – Distributes requests based on a key you define, such as the client IP address or
the request URL. NGINX Plus can optionally apply a consistent hash to minimize redistribution
of loads if the set of upstream servers changes.
  - *IP Hash* – The IP address of the client is used to determine which server receives the request.
Random with Two Choices – Picks two servers at random and sends the request to the
one that is selected by then applying the Least Connections algorithm (or for NGINX Plus
the Least Time algorithm, if so configured).

 ### Benefits of Load Balancing
 - Reduce do=wntime
 - Scalable
 - Redundancy
 - Flexibility
 - Efficiency


## PROXY SERVER 
-  A proxy server is a system or router that provides a gateway between users and the internet. Therefore, it helps prevent cyber attackers from entering a private network. It is a server, referred to as an “intermediary” because it goes between end-users and the web pages they visit online.
-  Because a proxy server has its own IP address, it acts as a go-between for a computer and the internet. Your computer knows this address, and when you send a request on the internet, it is routed to the proxy, which then gets the response from the web server and forwards the data from the page to your computer’s browser, like Chrome, Safari, Firefox, or Microsoft Edge.

  ### Proxy Servers and Network Security
  - Proxies provide a valuable layer of security for your computer. They can be set up as web filters or firewalls, protecting your computer from internet threats like malware.
  - This extra security is also valuable when coupled with a secure web gateway or other email security products. This way, you can filter traffic according to its level of safety or how much traffic your network—or individual computers—can handle.
  -  Some people use proxies for personal purposes, such as hiding their location while watching movies online, for example. For a company, however, they can be used to accomplish several key tasks such as:
   - Improve security
   - Secure employees’ internet activity from people trying to snoop on them
   - Balance internet traffic to prevent crashes
   - Control the websites employees and staff access in the office
   - Save bandwidth by caching files or compressing incoming traffic

![image](https://github.com/SourabhKumar2633/System-Design/assets/146738264/50b07b93-4fe0-42ae-b57b-d863aa995c48)
  - *How a Proxy Works*
    - Because a proxy server has its own IP address, it acts as a go-between for a computer and the internet. Your computer knows this address, and when you send a request on the internet, it is routed to the proxy, which then gets the response from the web server and forwards the data from the page to your computer’s browser, like Chrome, Safari, Firefox, or Microsoft Edge

  ### Benefits of a Proxy Server
  - *Enhanced security*: Can act like a firewall between your systems and the internet. Without them, hackers have easy access to your IP address, which they can use to infiltrate your computer or network.
  - *Private browsing, watching, listening, and shopping*: Use different proxies to help you avoid getting inundated with unwanted ads or the collection of IP-specific data. With a proxy, site browsing is well-protected and impossible to track.
  - *Access to location-specific content*: You can designate a proxy server with an address associated with another country. You can, in effect, make it look like you are in that country and gain full access to all the content computers in that country are allowed to interact with. For example, the technology can allow you to open location-restricted websites by using local IP addresses of the location you want to appear to be in. 
  - *Prevent employees from browsing inappropriate or distracting sites*: You can use it to block access to websites that run contrary to your organization’s principles. Also, you can block sites that typically end up distracting employees from important tasks. Some organizations block social media sites like Facebook and others to remove time-wasting temptations.

  ### Types of Proxy Servers
  - 1.Forward Proxy
       - A forward proxy sits in front of clients and is used to get data to groups of users within an internal network. When a request is sent, the proxy server examines it to decide whether it should proceed with making a connection.
       - A forward proxy is best suited for internal networks that need a single point of entry. It provides IP address security for those in the network and allows for straightforward administrative control. However, a forward proxy may limit an organization’s ability to cater to the needs of individual end-users.
  - 2.Transparent Proxy
       - A transparent proxy can give users an experience identical to what they would have if they were using their home computer. In that way, it is “transparent.” They can also be “forced” on users, meaning they are connected without knowing it.
       - Transparent proxies are well-suited for companies that want to make use of a proxy without making employees aware they are using one. It carries the advantage of providing a seamless user experience. On the other hand, transparent proxies are more susceptible to certain security threats, such as SYN-flood denial-of-service attacks.
  - 3.Anonymous Proxy
       - An anonymous proxy focuses on making internet activity untraceable. It works by accessing the internet on behalf of the user while hiding their identity and computer information.
       - A anonymous proxy is best suited for users who want to have full anonymity while accessing the internet. While anonymous proxies provide some of the best identity protection possible, they are not without drawbacks. Many view the use of anonymous proxies as underhanded, and users sometimes face pushback or discrimination as a result.
  - 4.High Anonymity Proxy
      - A high anonymity proxy is an anonymous proxy that takes anonymity one step further. It works by erasing your information before the proxy attempts to connect to the target site.
      - The server is best suited for users for whom anonymity is an absolute necessity, such as employees who do not want their activity traced back to the organization. On the downside, some of them, particularly the free ones, are decoys set up to trap users in order to access their personal information or data.
  -  5.Distorting Proxy
    - A distorting proxy identifies itself as a proxy to a website but hides its own identity. It does this by changing its IP address to an incorrect one.
    - Distorting proxies are a good choice for people who want to hide their location while accessing the internet. This type of proxy can make it look like you are browsing from a specific country and give you the advantage of hiding not just your identity but that of the proxy, too. This means even if you are associated with the proxy, your identity is still secure. However, some websites automatically block distorting proxies, which could keep an end-user from accessing sites they need.
  - 6.Data Center Proxy
    - Data center proxies are not affiliated with an internet service provider (ISP) but are provided by another corporation through a data center. The proxy server exists in a physical data center, and the user’s requests are routed through that server.
    - Data center proxies are a good choice for people who need quick response times and an inexpensive solution. They are therefore a good choice for people who need to gather intelligence on a person or organization very quickly. They carry the benefit of giving users the power to swiftly and inexpensively harvest data. On the other hand, they do not offer the highest level of anonymity, which may put users’ information or identity at risk.
  - 7.Residential Proxy
    - A residential proxy gives you an IP address that belongs to a specific, physical device. All requests are then channeled through that device.
    - A residential proxy gives you an IP address that belongs to a specific, physical device. All requests are then channeled through that device.
  - 8.Public Proxy
    - A public proxy is accessible by anyone free of charge. It works by giving users access to its IP address, hiding their identity as they visit sites.
    - Public proxies are best suited for users for whom cost is a major concern and security and speed are not. Although they are free and easily accessible, they are often slow because they get bogged down with free users. When you use a public proxy, you also run an increased risk of having your information accessed by others on the internet.
  - 9.Shared Proxy
     - Shared proxies are used by more than one user at once. They give you access to an IP address that may be shared by other people, and then you can surf the internet while appearing to browse from a location of your choice.
     - Shared proxies are a solid option for people who do not have a lot of money to spend and do not necessarily need a fast connection. The main advantage of a shared proxy is its low cost. Because they are shared by others, you may get blamed for someone else’s bad decisions, which could get you banned from a site.
 - 10.SSL Proxy
       - A secure sockets layer (SSL) proxy provides decryption between the client and the server. As the data is encrypted in both directions, the proxy hides its existence from both the client and the server.
       - These proxies are best suited for organizations that need enhanced protection against threats that the SSL protocol reveals and stops. Because Google prefers servers that use SSL, an SSL proxy, when used in connection with a website, may help its search engine ranking. On the downside, content encrypted on an SSL proxy cannot be cached, so when visiting websites multiple times, you may experience slower performance than you would otherwise.
  - 11.Rotating Proxy
       - A rotating proxy assigns a different IP address to each user that connects to it. As users connect, they are given an address that is unique from the device that connected before it.
       - Rotating proxies are ideal for users who need to do a lot of high-volume, continuous web scraping. They allow you to return to the same website again and again anonymously. However, you have to be careful when choosing rotating proxy services. Some of them contain public or shared proxies that could expose your data.
 - 12.Reverse Proxy
       - Unlike a forward proxy, which sits in front of clients, a reverse proxy is positioned in front of web servers and forwards requests from a browser to the web servers. It works by intercepting requests from the user at the network edge of the web server. It then sends the requests to and receives replies from the origin server.
       - Reverse proxies are a strong option for popular websites that need to balance the load of many incoming requests. They can help an organization reduce bandwidth load because they act like another web server managing incoming requests. The downside is reverse proxies can potentially expose the HTTP server architecture if an attacker is able to penetrate it. This means network administrators may have to beef up or reposition their firewall if they are using a reverse proxy.


## NAT (Network Address Translation)
- A Network Address Translation (NAT) is the process of mapping an internet protocol (IP) address to another by changing the header of IP packets while in transit via a router. This helps to improve security and decrease the number of IP addresses an organization needs.
- A NAT works by selecting gateways that sit between two local networks: the internal network, and the outside network. Systems on the inside network are typically assigned IP addresses that cannot be routed to external networks (e.g., networks in the 10.0.0.0/8 block).
- A few externally valid IP addresses are assigned to the gateway. The gateway makes outbound traffic from an inside system appear to be coming from one of the valid external addresses. It takes incoming traffic aimed at a valid external address and sends it to the correct internal system.
- This helps ensure security. Because each outgoing or incoming request must go through a translation process that offers the opportunity to qualify or authenticate incoming streams and match them to outgoing requests
- For Example- NAT conserves the number of globally valid IP addresses a company needs and -- in combination with Classless Inter-Domain Routing (CIDR) -- has done a lot to extend the useful life of IPv4 as a result. NAT is described in general terms in IETF RFC 1631.
  ### What are the various types of NAT techniques?
  - The NAT mechanism ("natting") is a router feature, and is often part of a corporate firewall. NAT gateways can map IP addresses in several ways:
    - from a local IP address to one global IP address statically;
    - hiding an entire IP address space comprised of private IP addresses behind a single IP address;
    - to a large private network using a single public IP address using translation tables;
    - from a local IP address plus a particular TCP port to a global address or a pool of public IP addresses; and
    - from a global IP address to any of a pool of local IP addresses on a round-robin basis.
  - In some cases, network administrators define policies that allow the gateway device to assign mappings based on the intended destination ("pick this external address for communications to partner A's area network; pick that external address for communications to partner B's").
  - Policies can also be used on the protocols being used ("assign out of this pool for HTTP traffic, that pool for HTTPS") or on other factors.
  -  A newer way to use NAT focuses on translating an ISP provider's IPv4 addresses to IPv6, and vice versa. This provides integration of IPv4 infrastructure and end nodes into IPv6 environments, and allows IPv6 services to interact with IPv4 systems.
 ### What is the difference between dynamic NAT (DNAT) and static NAT (SNAT)?
 - A dynamic NAT is common in larger organizations with complex internal networks. It uses several available IP addresses during the translation.
 - An example of this can be seen with Cisco, which has developed a technique that uses a NAT overload to map several private IP addresses to a single public IP address.
 - Conversely, a static NAT, also common in large organizations, provides a 1:1 mapping between an internal IP address and a public network IP address.

 ### NAT64 
 - NAT64 is an IPv6 transition technology that supports the translation of an IPv6 network address into an IPv4 address.
 - There are stateless and stateful versions of NAT64:
   - *Stateless NAT64*: This mechanism is stateless because it doesn't maintain any bindings or session state while performing address translation, and it supports both IPv6-initiated and IPv4-initiated communications. (A binding is a one-to-one association between a private IP address and its translated public IP address.)
   - *Stateful NAT64*: This mechanism is stateful because it creates or modifies session state or bindings while performing address translation. Stateful NAT64 supports both IPv6-initiated and IPv4-initiated communications using static or manual mappings.

 ### What are application-level gateways (ALGs)?
 - Application-level gateways are applications that translate IP address information inside the payload of an application packet. They can be used to perform NAT and firewall actions, depending on configurations.
 - ALGs that are configured to perform NAT and firewall actions can:
   - Allow client applications to use dynamic TCP or UDP ports to communicate with a server app
   - Recognize application-specific commands and offer granular security control over those commands
   - Synchronize multiple streams or sessions of data between two hosts that are exchanging data
   - Translate network-layer address information available in an application's payload
 ### ALG: A helper for NAT
 - Not all internet protocols carry source and destination IP addresses in an application data stream. Examples include HTTP, Network Time Protocol (NTP), remote login (rlogin), and remote copy (rcp). NAT can perform translation services on these types of protocols.
 - However, NAT needs ALG support when it encounters specific protocols that embed IP address information within the payload. In fact, NAT requires various ALGs to handle application data stream (Layer 7) protocol-specific services, such as translating embedded IP addresses and port numbers in the packet payload and extracting new connection and session information from control channels.
 - ALG also supports stateful NAT translation. For example, Session Initiation Protocol (SIP) files must be handled with special care when translated because they have control and data communication components associated with the same user transaction. These files can signal to routers when to set up voice and multimedia over IP networks.
 - An ALG needs to be used with NAT to translate the embedded protocol messages and keep the control and data components bound together.
### Carrier-grade NAT
- Carrier-grade network address translation, known also as CGN or CGNAT, translates IP addresses at a much larger scale, often handling tens of millions NAT translations. Service providers and companies with large-scale networks rely on CGN for internet and cloud connectivity. As a result, CGN should be supported by a capable platform that can serve high-scale demands.
### NAT444 for service providers
- Service providers using CGN may also employ a NAT444 architecture as a strategy to manage a waning IPv4 supply.
- With NAT444, customer connections to internet services and the cloud can pass through three different IPv4 addressing domains: the customer's private network, the carrier's private network, and the public internet.
### NAT High Availability (HA)
- *Stateless and stateful NAT HA*
  - When a standby NAT router or edge platform is unaware of the translations that an active NAT router or edge platform performs, it's called stateless redundancy.
  - Stateless NAT HA provides fast switchover between active and standby routers due to faults that may occur in any part of the network. With stateless HA, the applications traffic has to re-create NAT translation in a new active router.
  - With stateful NAT HA, a standby router or edge platform knows all the translations that the active NAT router is performing. If an adverse event impacts the active router and traffic must switch to the standby router, then the standby router won't need to re-create the translation. This enables sessions to continue sending traffic from new active router.
### High-speed logging
- Today's NAT technology can support high-speed logging (HSL) for multiple destinations. And leading NAT solutions can support tens of millions of translations on one data plane. This type of speed and volume for message logging isn't possible using the traditional syslog logging standard.
- HSL, when configured, can enable NAT to provide a log of the packets flowing through routing devices to an external collector. Records are sent for each binding created by NAT and also when sessions are created or destroyed. The session records include necessary tracking information such as source IP address, destination IP address, source port, destination port, and protocol information, and more importantly, event time and type.
- NAT high-speed logging records can be invaluable documentation for investigations of illegal or other malicious or problematic activity on a network
### How can NAT help transition to IPv6?
- While IPv6 offers a large number of IP address space to fulfill increasing host demands in today's networks, chances are you need IPv6 and IPv4 addresses to coexist in your network.
- NAT can help support this coexistence and transition, allowing IPv6-only devices to communicate with IPv4-only devices and vice versa. NAT allows organizations to connect IPv6 and IPv4 networks using NAT64 translations.
- As a networking service, it's important that NAT is supported with underlay performance.


## Public & Private DNS
-*Public DNS*: Public DNS servers are available to anyone on the internet and are provided by companies such as Google, OpenDNS, and Cloudflare. They can be used to resolve domain names to IP addresses for any website on the internet. Public DNS servers are typically faster and more reliable than those provided by ISPs, and they often offer additional features such as security and ad-blocking.
-*Private DNS*: Private DNS servers, on the other hand, are used within a specific organization or network. They are typically used in enterprise or home networks to resolve domain names internally, rather than on the public internet. For example, a company might use a private DNS server to map internal hostnames to IP addresses, or a user might set up a private DNS server on their home network to block ads and improve privacy.
## VPN
-### What should a good VPN do?
 -*Encryption of your IP address*: The primary job of a VPN is to hide your IP address from your ISP and other third parties. This allows you to send and receive information online without the risk of anyone but you and the VPN provider seeing it.
 -*Encryption of protocols*: A VPN should also prevent you from leaving traces, for example, in the form of your internet history, search history and cookies. The encryption of cookies is especially important because it prevents third parties from gaining access to confidential information such as personal data, financial information and other content on website
 -*Kill switch*: If your VPN connection is suddenly interrupted, your secure connection will also be interrupted. A good VPN can detect this sudden downtime and terminate preselected programs, reducing the likelihood that data is compromised.
 -*Two-factor authentication*: By using a variety of authentication methods, a strong VPN checks everyone who tries to log in. For example, you might be prompted to enter a password, after which a code is sent to your mobile device. This makes it difficult for uninvited third parties to access your secure connection.

### Types of VPN 
  - SSL VPN
    - The prerequisite is usually an HTML-5-capable browser, which is used to call up the company's login page. HTML-5 capable browsers are available for virtually any operating system. Access is guarded with a username and password.
  - Site-to-site VPN
    -A site-to-site VPN is essentially a private network designed to hide private intranets and allow users of these secure networks to access each other's resources.
    - A site-to-site VPN is useful if you have multiple locations in your company, each with its own local area network (LAN) connected to the WAN (Wide Area Network). Site-to-site VPNs are also useful if you have two separate intranets between which you want to send files without users from one intranet explicitly accessing the other.
  - Client to server VPN
    - This involves the user not being connected to the internet via his own ISP, but establishing a direct connection through his/her VPN provider. This essentially shortens the tunnel phase of the VPN journey. Instead of using the VPN to create an encryption tunnel to disguise the existing internet connection, the VPN can automatically encrypt the data before it is made available to the user.
    - This is an increasingly common form of VPN, which is particularly useful for providers of insecure public WLAN. It prevents third parties from accessing and compromising the network connection and encrypts data all the way to the provider. It also prevents ISPs from accessing data that, for whatever reason, remains unencrypted and bypasses any restrictions on the user's internet access (for instance, if the government of that country restricts internet access).

## IPv4 & IPv6
- Internet Protocol version 4 (IPv4) is the fourth version of the Internet Protocol (IP). It is one of the core protocols of standards-based internetworking methods in the Internet and other packet-switched networks. IPv4 was the first version deployed for production on SATNET in 1982 and on the ARPANET in January 1983. It is still used to route most Internet traffic today,[1] even with the ongoing deployment of Internet Protocol version 6 (IPv6),[2] its successor.
- https://en.m.wikipedia.org/wiki/File:IPv4_Packet-en.svg

- IPv4 uses a 32-bit address space which provides 4,294,967,296 (232) unique addresses, but large blocks are reserved for special networking purposes
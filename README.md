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
    - 5.Distorting Proxy
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
       - 8.Shared Proxy
         - Shared proxies are used by more than one user at once. They give you access to an IP address that may be shared by other people, and then you can surf the internet while appearing to browse from a location of your choice.
         - Shared proxies are a solid option for people who do not have a lot of money to spend and do not necessarily need a fast connection. The main advantage of a shared proxy is its low cost. Because they are shared by others, you may get blamed for someone else’s bad decisions, which could get you banned from a site.
        - 9.SSL Proxy
          - A secure sockets layer (SSL) proxy provides decryption between the client and the server. As the data is encrypted in both directions, the proxy hides its existence from both the client and the server.
          - These proxies are best suited for organizations that need enhanced protection against threats that the SSL protocol reveals and stops. Because Google prefers servers that use SSL, an SSL proxy, when used in connection with a website, may help its search engine ranking. On the downside, content encrypted on an SSL proxy cannot be cached, so when visiting websites multiple times, you may experience slower performance than you would otherwise.
       - 10.Rotating Proxy
          - A rotating proxy assigns a different IP address to each user that connects to it. As users connect, they are given an address that is unique from the device that connected before it.
          - Rotating proxies are ideal for users who need to do a lot of high-volume, continuous web scraping. They allow you to return to the same website again and again anonymously. However, you have to be careful when choosing rotating proxy services. Some of them contain public or shared proxies that could expose your data.
        - 11.Reverse Proxy
          - Unlike a forward proxy, which sits in front of clients, a reverse proxy is positioned in front of web servers and forwards requests from a browser to the web servers. It works by intercepting requests from the user at the network edge of the web server. It then sends the requests to and receives replies from the origin server.
          - Reverse proxies are a strong option for popular websites that need to balance the load of many incoming requests. They can help an organization reduce bandwidth load because they act like another web server managing incoming requests. The downside is reverse proxies can potentially expose the HTTP server architecture if an attacker is able to penetrate it. This means network administrators may have to beef up or reposition their firewall if they are using a reverse proxy.




  

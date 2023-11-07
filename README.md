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


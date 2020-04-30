# Remaining

# Articles: 

https://medium.com/system-designing-interviews/approach-a-system-design-interview-f3594e243730


# videos

Distributed database: 
https://interviewing.io/recordings/Systems-Design-Google-15/

Tech lead video:  
https://www.youtube.com/watch?v=REB_eGHK_P4

Tushar video:  
https://www.youtube.com/watch?v=UzLMhqg3_Wc

LRU cache: 
https://interviewing.io/recordings/Javascript-Pivotal-Labs-1/

13 systems design videos on history.  

Remaining:   
- 4/1/20: Social Media sharing: er: Tea-Smoked Slide Rule.  
- 3/23/20: Webcrawler. ee: Tea-Smoked Slide Rule. er: Invincible Cloud.  
- 3/29/20: leetcode.  
- 12/30/2019(failed)messenger application er: Eponymous Lambda ee: Wandering Porpoise.  
- 12/22/2019 (Failed): Stocks er: Eponymous Lambda.  
- 12/22/2019(Failed): Amazon e-commerce Application er: Ubiquitous Goblin  



- (rewatch)11/12/2019: The Benevolent Donut, pizza delivery with the highschooler


13- 3/16/2019: Distributed Caching System.  

somewhat:  
- 3/26/2020 (X): very low volume, design photo storage system.   
10- 10/16/2019: Interviewed by Engineering manager at large company. 18 years experience, 4 years in management. Wunderground, weather unground (Interviewer is not good).   

OO design:  
- 11/19/2019: The Benevolent Donut, design API for game of checker

Useless: 
11- 8/18/2019: Design what's app. Interviewer: Teflon Enigma (not good).  
12- 7/8/2019 (failed, not much useful): Pizza Ordering App   Interviewee: Teflon Enigma (not good)   


# Object oriented design: 
- Mine Sweeper
- Parking Lot
- 

# Rest: 
http://dummy.restapiexample.com/

# CAP Thereom:  
Consistency, Availability, Partition tolerance.  

Consistency: Every read is guaranteed to return the most recent write or an error.  
Availability: Every request receives a non-error response from a non-failing node in a reasonable time. It is expected that the client may not receive the most recent write.  
Partition tolerance: The system continues to operate when network partition happens.  

Given that networks aren't completely reliable, you must tolerate partitions in a distributed system.   
you get to choose what to do when a partition does occur. According to the CAP theorem, this means we are left with two options: Consistency and Availability.   

CP - Consistency/Partition Tolerance - Wait for a response from the partitioned node which could result in a timeout error. The system can also choose to return an error, depending on the scenario you desire. Choose Consistency over Availability when your business requirements dictate atomic reads and writes.

AP - Availability/Partition Tolerance - Return the most recent version of the data you have, which could be stale. This system state will also accept writes that can be processed later when the partition is resolved. Choose Availability over Consistency when your business requirements allow for some flexibility around when the data in the system synchronizes. Availability is also a compelling option when the system needs to continue to function in spite of external errors (shopping carts, etc.)

More info: https://robertgreiner.com/cap-theorem-revisited/

# mTLS:
What is mTLS?   
Mutual TLS (Transport Layer Security).  
Difference between TLS and mTLS.  

# Cheat sheet: 
### Handy conversion guide:

2.5 million seconds per month.  
1 request per second = 2.5 million requests per month.  
40 requests per second = 100 million requests per month.  
400 requests per second = 1 billion requests per month.  

### Load balancer: 
Nginx, HAProxy, DNS (domain name to multiple ip addresses, more limited for customization)

types of load balancing: Round robin, machine with least load, hashing on the ip address

### Push notification: 
Client pull or server push.  

Server push: Websocket (more common), SSE (Server Sent Events)

### caching: 
to offload the traffic from the DB.  

Different caches: redis, memcached

### distributed file system: 
S3  
For example allow users to store images.  

### type of databases: 

nosql: Amazon DynamoDB, mongoDB, Firebase Firestore

#### relational database scaling: 
vertical: multiple tables, each table in one machine. Like Users table, tweets in different machines. 
horizontal: tweet table itself is huge, needes more than one machine. Use more than one machine. Hash mod technique. hash of the user id mod number of servers used for the tweets table. 

#### mysql master slave: 
write to master,    
read from slaves

### Topics to mention: 
CAP Theorem  
Back of the envelop calculation.   
Security.   
CDN (for static content like javascript, images)


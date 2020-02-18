The following set of steps happen when you type a URL in a browser.

1. **The browser checks the cache for a DNS record to find the address of example.com**       
    a. The DNS (Domain Name System) is a database, essentially a hashmap. { IPAddress: Friendly name}      
    b. IP address belongs to the computer that hosts the server of the website.      
    c. So, what's the point of a DNS? - Human friendly navigation; it just is easier to remember a human friendly name.      
    
 2. **So how does the it find the DNS record?**       
    a. To find the DNS record, it checks four caches.
    b. First - *Browser Cache*: Browser maintains a repository of DNS records for a fixed duration for websites previously visited.      
    c. Second - *OS Cache*: The browser can make a system call to search for the DNS cache, that is kept locally.            
    d. Third - *Router Cache*: If it's not in the computer; next - the router's cache will be checked.          
    e. Fourth - *ISP Cache*: If all the above steps fail, the browser will move on to the ISP. The ISP has it's own DNS server which
       includes a cache of DNS records?      
       
Caches are vital for regulating network traffic and improving data transfer times.       

3. If the requested URL is not in the cache, ISP's DNS server intiates a DNS query to find the IP address of the server <example.com>   
    a. This type of search is called *resursive search* that will repeatedly search, until we get the mapping (or) error response.     
    b. We would be calling the ISP's DNS server - DNS recursor, whose responsibility is to find the poper IP address.     
        1. It will ask other DNS servers on the internet for the mapping.     
        2. The other DNS servers are called - 'name servers'; since they perform DNS search based on the domain architecture of the domanin name.
        3. Remember? -- Root Domain, Top-Level Domains, Second-Leve Domains, Third-Level Domains...              
        4. These requests are sent using small data packets that contain information such as content of the request and the IP address.   
        5. Here routing tables are used to figure out which way is the fastest possible for the packet to reach its detination.    
        
**OK, we now, have the mapping -- So what happens now??**     

The browser initiates a **TCP connection** with the server.

1. Once we have the IP-Address, the browser initiates a TCO connection with the server.    
2. TCP is the most common protocol for many type of HTTP requests.    
3. To transfer packets between your client and the server, the TCP connection is established using TCP/IP - three way handshake.    


**So What is the TCP 3 way hand-shake??**
1. The client machine sends a SYN packet to the server over the internt, asking if it is open for new connections.   
2. If the server has open ports, that can accept and initiate new connections, it will respond using a ACK for the SYN packet using a SYN/ACK packet.      
3. The client will recieve the SYN/ACK packet from the server and will acknowledge it by sending an ACK packet.     

Hence, the TCP connection is established for data transmission.       

**After TCP connection is established**
*The browser sends an HTTP request to the webserver*

1. Since the TCP connections is established it is time to start transferring data.
2. The browser will send a `GET` request (or) `POST` request. 
3. This request will also contain additional information such as the brwoser identitication (User-Agent) header; types of requests (Accept Header), and Connection Header - "keep-alive"; to keep the TCP connection alive. 

**Server handles the request and sends back a response**    
1. The server contains a webserver, that recieves the request and passes it to a request handler to read and generate a response.
2. request handler - is a ruby / python script - response can be a JSON, XML or HTML payload.      


The server sends out a HTTP response.      
1. The server response contains:
    a. Web-Page that we requested.       
    b. Compression type (Content-Encoding)     
    c. Any cookies to set?     
    d. Privacy Information   
    
  
Finally,     

1. The browser displays the HTML content in phases. First it will render bare bon HTML skeleton.    
2. Check HTML tags, and send out GET requests      That's it!!!








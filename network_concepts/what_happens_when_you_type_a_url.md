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

The browser initiates a TCP connection with the server.

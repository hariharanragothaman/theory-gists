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
       

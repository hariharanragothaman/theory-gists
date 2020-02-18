This explains how TCP-IP 3 way handshake works.

Some important points to note:
1. TCP provides reliable communication with **Positive Acknowledgement with Re-Transmission**
2. The [Protocol-Data-Unit] of this transport layer is called segment.
3. When using 'PAR',  the data is re-sent, until an acknowledgement is recieved. 
4. So the sender has to "re-send" data for which the PAR is not recieved. 

The steps are as follows:

1. (SYN): Client wants to establish a connection with the server. 
  a. Client sends a segment with SYN (Sycnhoronize Sequence Number) which informs the server that client is going to start communication.    
  b. Also with what sequence number it starts?   
2. (SYN+ACK): Server responds to the client request with SYN-ACK signal bits set.    
  a. ACK signifies the response of the segment it received and SYN signifies the sequence number it ls like to start with      
3. (ACK): - Final acknowledgement that client initiates, for response of the server. which starts the data-transfer.    


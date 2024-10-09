# DNS_practice
<h1>Practicing DNS</h1>
<img src= "https://github.com/user-attachments/assets/8e1e4d26-506a-49ea-97c5-09f86ad0e43b" width="400" />

<h2>A-Record Exercise</h2>

![image](https://github.com/user-attachments/assets/ea4d1958-dbe8-4bdd-aebb-74e9e97b7155)
![image](https://github.com/user-attachments/assets/2b9769e0-3d39-4fb8-90ac-2eacddc44f69)

- reconnect to both of my Virtual Machines(DC-1 and Client-1)
- From Client-1 tried to ping “mainframe” notice that it fails
- Nslookup “mainframe”  it fails (no DNS record)

  
- Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
- Go back to Client-1 and try to ping it. Observe that it works

<h2>Local DNS Cache Exercise</h2>
- Go back to DC-1 and change mainframe’s record address to 8.8.8.8
- Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
- Observe the local dns cache (ipconfig /displaydns)
- Flush the DNS cache (ipconfig /flushdns).
- Observe that the cache is empty (ipconfig /displaydns)
- Attempt to ping “mainframe” again. Observe the address of the new record is showing up

<h2>CNAME Record Exercise</h2>
- Go back to DC-1 and create a CNAME record that points the host “search” to “www.google.com”
- Go back to Client-1 and attempt to ping “search”, observe the results of the CNAME record
- On Client-1, nslookup “search”, observe the results of the CNAME record


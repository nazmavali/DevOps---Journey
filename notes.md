\# My Notes



\## Networking

\- **IP address**	Computer's address	A unique number that identifies a device on a network, so data can be sent to it.



\-**ipconfig**	Shows the computer's address card	A Windows command that shows the network configuration: IP address, subnet mask, and default gateway.



\-**ping**	Checks if another computer answers	A command that tests whether a device is reachable over the network, and measures the round-trip time (how long a message takes to go there and come back).





nazma@NazmaVali MINGW64 \~/DevOps-Journey (main)

$ ping amazon.com



Pinging amazon.com \[98.87.170.71] with 32 bytes of data:

Request timed out.

Request timed out.

Request timed out.

Request timed out.



Ping statistics for 98.87.170.71:

&#x20;   Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),



nazma@NazmaVali MINGW64 \~/DevOps-Journey (main)

$ ping facebook.com



Pinging facebook.com \[2a03:2880:f366:1:face:b00c:0:25de] with 32 bytes of data:

Reply from 2a03:2880:f366:1:face:b00c:0:25de: time=27ms

Reply from 2a03:2880:f366:1:face:b00c:0:25de: time=26ms

Reply from 2a03:2880:f366:1:face:b00c:0:25de: time=35ms

Reply from 2a03:2880:f366:1:face:b00c:0:25de: time=30ms



Ping statistics for 2a03:2880:f366:1:face:b00c:0:25de:

&#x20;   Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

&#x20;   Minimum = 26ms, Maximum = 35ms, Average = 29ms





nazma@NazmaVali MINGW64 \~/DevOps-Journey (main)

$



* ping results:

&#x20; - Reply + small time + Lost 0 = working

&#x20; - Request timed out = no answer. It might be down, or it might just block ping (like amazon.com)

&#x20; - Near computers answer faster (my router: 4ms). Far ones are slower (google: 47ms)







\- DNS: turns a website name into an IP address

\- nslookup: asks DNS for a name's IP address

* tracert: shows every stop my message takes to reach a website. Stop 1 is my router, the last stop is the destination.



* port: a number that tells a computer which service a message is for. IP address finds the computer, port finds the service.
* \- common ports: 22 = SSH (login), 80 = HTTP (website), 443 = HTTPS (secure website)
* \- netstat -an: shows the ports my computer is using. LISTENING = door open, waiting. ESTABLISHED = talking right now.





\- HTTP: the rules for a browser to ask a website for a page (request) and get an answer (response)

\- HTTPS: same as HTTP but secure (S for Secure). Port 443. HTTP is port 80.

\- curl -I: shows the top of a website's answer. Hook: "browser with only text"

\- Status codes: 200 = worked, 404 = wrong page, 500 = the website is broken



## Week 2 Summary: Networking basics

\- ipconfig: my computer's address settings ("my ID card")

\- ping: checks if another computer answers ("are you there?")

\- nslookup: asks DNS for a name's IP address ("name to number")

\- tracert: every stop my message takes to a website ("trace the route")

\- netstat -an: ports my computer is using ("which doors are open")

\- curl -I: top of a website's answer ("browser with only text")

\- Ports: 22 = SSH (login), 80 = HTTP, 443 = HTTPS (S for Secure)

\- Status codes: 200 = worked, 404 = wrong page, 500 = website is broken

\- Typing google.com: DNS turns the name into an IP first, then it connects



\## Subnets

\- subnet: a smaller group of computers inside a bigger network ("one floor")

\- /24 = 255.255.255.0: first 3 numbers are the floor, last number is the computer

\- a /24 subnet holds 254 computers

\- naming a floor: keep first 3 numbers, last becomes 0, add /24. Example: 10.0.0.61 -> 10.0.0.0/24

\- my home Wi-Fi floor: 10.0.0.0/24. VirtualBox floor: 192.168.56.0/24


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


- ping results:

&#x20; - Reply + small time + Lost 0 = working

&#x20; - Request timed out = no answer. It might be down, or it might just block ping (like amazon.com)

&#x20; - Near computers answer faster (my router: 4ms). Far ones are slower (google: 47ms)


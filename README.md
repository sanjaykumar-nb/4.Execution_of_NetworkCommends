# 4.Execution_of_NetworkCommands
## AIM :
Use of Network commands in Real Time environment
## Software :
Command Prompt And Network Protocol Analyzer
## Procedure:
To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## program
```
client
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
server
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
trace route
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```

## Output
## trace:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/80b4d147-6236-4517-b473-c57f5c03e000)

## ping:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/a8d70a7c-1a49-40b3-90f3-837b1601b7ba)

## ipconfig/all:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/e9ed219b-9640-4122-a203-07e2d168099c)

## netstat-ano:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/b159bf37-860d-4fc8-873e-6cb37d960454)

## nslookup:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/0427bfd7-a843-4f05-af2b-60e5ce84edde)

## curl:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/de8608e4-d526-49c1-a1f0-8b985bd6190d)

## ftp:
![image](https://github.com/sanjaykumar-nb/4.Execution_of_NetworkCommends/assets/154039979/013f840a-b462-45cf-bcb6-63db11ca0d83)

## Result
Thus Execution of Network commands Performed 

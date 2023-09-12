# Quiz 73

Create a simple program to manage a network routing table. A routing table is used by network devices, like routers, to determine where to send data based on MAC addresses. Your program will help manage the mapping between MAC and IP addresses.


## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9477.JPG)

<sub>Fig.1 shows the working on paper


## Code

```py
import random
def check_mac(mac):
    return len(mac) == 17 and mac.count(":") == 5

def generate_ipv4():
    ipv4 = ".".join(str(random.randint(0, 255)) for a in range(4))
    return ipv4

def update(table, mac):
    if check_mac(mac):
        if mac in table:
            return table[mac]
        else:
            while True:
                ip = generate_ipv4()
                if ip not in table.values():
                    table[mac] = ip
                    return ip

def display(table):
    print("Routing Table:")
    for mac, ip in table.items():
        print(f"MAC: {mac}, IP: {ip}")

table = {}
while True:
    mac_address = input("Enter MAC address: ")
    ip_address = update(table, mac_address)
    display(table)
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-13%20at%2000.17.36.png)

<sub>Fig.2 shows the results of the program

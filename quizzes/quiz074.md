# Quiz 74

A data package is build by splitting the data into fixed sizes (load) and attach a header which contains the MAC address, IP address of the sender (sx) and destination (rx), and a sequence number to reconstruct the data. Create the function below:


## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9478.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
def data_package(macrx, IP_rx, mac_sx, IP_sx, data):
    list = []
    final = f"{macrx}|{IP_rx}|{mac_sx}|{IP_sx}|"
    count = 0
    if len(data) % 4 == 0:
        for i in range(len(data) // 4):
            total = final + f"{data[count:(count + 4)]}"
            list.append(total)
            count += 4
    else:
        for i in range((len(data) // 4) + 1):
            total = final + f"{data[count:(count + 4)]}"
            list.append(total)
            count += 4
    return list

macrx = input("Macrx: ")
IP_rx = input("IP_rx: ")
mac_sx = input("Mac_sx: ")
IP_sx = input("IP_sx: ")
data = input("Data: ")
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-13%20at%2000.56.09.png)

<sub>Fig.2 shows the results of the program

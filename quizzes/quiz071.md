# Quiz 71

Create the code for the IPv6 machine

## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9475.jpg)

<sub>Fig.1 shows the working on paper

## Code

```py
from random import randint
def ipv6machine(N: int):
    ipv6_list = []
    for i in range(N):
        ipv6_address = ""
        for a in range(8):
            eachone = ""
            hex = ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "A", "B", "C", "D", "E", "F"]
            for b in range(4):
                x = randint(0, 15)
                eachone += hex[x]
            ipv6_address += eachone
            if a != 7:
                ipv6_address += ":"
        ipv6_list.append(ipv6_address)
    return ipv6_list
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-12%20at%2023.28.12.png)

<sub>Fig.2 shows the results of the program

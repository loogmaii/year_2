# Quiz 72

Create the code for the MAC generator machine

## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9476.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
import random
def macGenorator(N:int):
    hex = ['0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F']
    listmac = []
    for i in range(N):
        mac = ''
        for i in range(6):
            for i in range(2):
                mac += hex[random.randint(0,15)]
            mac += ":"
        listmac.append(mac)
    return listmac
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-12%20at%2023.33.58.png)

<sub>Fig.2 shows the results of the program

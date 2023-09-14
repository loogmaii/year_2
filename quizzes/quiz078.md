# Quiz 78

The layer in the OSI model that adds the port number to the header is the Transport Layer, which is Layer 4 in the OSI model. Create a Layer 4 firewall which only allows connections in Port 80 and 22123. Assume the first 16 bits of the input string are used for the port number.

## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9494.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
def firewall(data):
    if len(data) < 16:
        return  ""

    bits = data[:16]
    num = int(bits, 2)

    if num == 80 or num == 22123:
        return "Allowed", data[16:]
    else:
        return "Filtered", ""
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-14%20at%2009.55.42.png)

<sub>Fig.2 shows the results of the program

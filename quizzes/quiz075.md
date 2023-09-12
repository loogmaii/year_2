# Quiz 75

Physical Layer of the OSI model primarily deals with the physical aspects of data transmission, including the hardware, transmission medium (cable, waves, etc), encoding, signaling, and synchronization necessary to send raw bits between devices.

Create a function that converts the input:str to a binary:str


## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9479.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
def convert(message:str):
    product = ""
    for i in message:
        binary = ''
        n = ord(i)
        while n>0:
            res=n%2
            binary = str(res) + binary
            n = n//2
        while len(binary)<8:
            binary = '0'*(8 - len(binary)) + binary
        product += f"{binary} "
    return product.strip()
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-13%20at%2001.07.04.png)

<sub>Fig.2 shows the results of the program

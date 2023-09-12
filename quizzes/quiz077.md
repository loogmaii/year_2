# Quiz 77

Physical layer is also in charge of detecting and trying to correct errors in the data transmitted. Create a function to checks the parity bit of a data string, and determine if there is an error. Assume parity=1 for even number of ones


## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9481.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
def check_error2(data):
    error = False
    n = int(data[0])
    count = 0
    for i in range(1, len(data)):
        count += int(data[i])
    if count % 2 == 0 and n == 1:
        error = False
    elif count % 2 == 1 and n == 0:
        error = False
    else:
        error = True
    return error
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-13%20at%2001.45.08.png)

<sub>Fig.2 shows the results of the program

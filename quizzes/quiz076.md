# Quiz 76

Physical layer is also in charge of detecting and trying to correct errors in the data transmitted. One simple way would be to send copies of the data and check that the copies match. Assume the data is 2 copies of the data plus original.


## Working on paper

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/IMG_9480.jpg)

<sub>Fig.1 shows the working on paper


## Code

```py
def check_error(data):
    error = ""
    data_len = len(data)
    a = data[0:data_len // 3]
    b = data[data_len // 3:(data_len * 2) // 3]
    original = data[(2 * data_len) // 3:]
    if a == b == original:
        error = False
    else:
        error = True
    return error

test1 = check_error("100111001011001110010110011100101")
print(test1)
test2 = check_error("011101111101110111110111001111")
print(test2)
```

## Evidence

![](https://github.com/loogmaii/year_2/blob/main/quizzes/images/Screenshot%202566-09-13%20at%2001.28.07.png)

<sub>Fig.2 shows the results of the program

Task 1
Program that prints 100 bears with special case taken in account:
```.py
def draw():
    fill(255)
    for b in range (0, 100):
        if b == 1:
            b = str(b)
            print (b + " bear")
        b = str(b)
        print (b + " bears")
```

Task 2
Program that prints the years from 1900 to 2000:
```.py
def draw():
    fill(255)
    for y in range (1900, 2001):
        y = str(y)
        print ("The year is " + y)
```

Task 3
Program that prints the conversion for Celsius to Fahrenheit from 0 C to 100 C:
```.py
def faren(cel):
    cel = int(cel)
    far = (cel * 9/5) + 32
    return far

def draw():
    global far
    fill(255)
    for cel in range (101):
        far = faren(cel)
        far = str(far)
        cel = str(cel)
        print (cel + " C are " + far + " F")
```

Simulation tasks 1 and 2:
```.py
```

Simulation task 3:
https://docs.google.com/presentation/d/1oTZ9i8UyLfqGo1bb4ezR2mchyo0E4Owbq6-zbmTdDEE/edit?usp=sharing

Simulation task 4:


Simulation task 5:

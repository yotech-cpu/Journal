Q.1 What did we do?
We continued with our simulation and have tested out the effects of different amounts of interactions in a virus breakout. Apart from our progress with the Processing simulation, we tested our knowledge on the for loop through a couple of tasks.

Q.2 What did I learn?
I learnt more about the for loop which I would say has tested a lot of previous concepts we have learnt in class as well. I also had a more visual learning of how different factors can have a direct impact on the spread of a virus.

Q.3 What questions do I have?
How can I improve on the efficiency of my program in terms of reducing the computer operations required for the code to run and thus, making the software lighter.
I observed that sometimes the results didn't come out as expected, especially for task 5 of the simulation table. Is it better to take multiple runs and use the mean? If so, how many times should be run the program?

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
x = [100]
y = [100]
people = 20
count = 0
infected = 0
infectedx = 0
healthy = people
healthyx = 0
h = [False, True]

def setup():
    global people, infected, healthy
    size(500,500)
    for n in range(people):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append(True)

def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c

def draw():
    global x, people, h, y, count, infected, healthy, infectedx, healthyx
    health = []
    background(255)
    for ind in range(len(x)):
        if h[ind] == True:
            fill(255)
        else:
            fill(255,0,0)
        health.append(h[ind])
        #print health
        circle(x[ind], y[ind], 40)
        for nei in range(len(x)):
            if nei == ind:
                continue
            d = distance(x[ind], x[nei], y[ind], y[nei])
            if d < 40 and (h[nei] == False or h[ind] == False):
                h[ind] = False
                h[nei] = False
        healthy = sum(health)
    for m in range(len(x)):
        x[m] += random(-20, 20)
        y[m] += random(-20, 20)
        if x[m] > 500:
            x[m] = 500
        elif x[m] < 0:
            x[m] = 0
        elif y[m] > 500:
            y[m] = 500
        elif y[m] < 0:
            y[m] = 0
    count += 1
    healthy = sum(health)
    infected = 1 + (people - healthy)
    healthyx = healthy * 8
    infectedx = infected * 8
    textSize(20)
    fill(0)
    text("Run: ", 400, 20)
    text(count, 450, 20)
    textSize(15)
    text("Infected", 250, 460)
    text("Healthy", 250, 480)
    text(infected, 480, 460)
    text(healthy, 480, 480)
    fill(255,0,0)
    rect(320,450,infectedx,10)
    fill(255)
    rect(320,470,healthyx,10)
    if infected == people + 1:
        print count
    delay(50)
```

Simulation task 3 and 5:
https://docs.google.com/presentation/d/1oTZ9i8UyLfqGo1bb4ezR2mchyo0E4Owbq6-zbmTdDEE/edit?usp=sharing

Simulation task 4:
We can conclude that the number of people moving is more or less inversely proportional to the number of iterations until all population is infected. We see that because as the movement reduces, the number of iterations until all population is infected increases

Short Questions about the e-learning:
1. How is the e-learning format working for you in our class?
It's very useful to have tutorial videos and tasks. It's helped me learn a lot and not just about programming in processing.

2. Is the load sufficient/overwhelming?
I feel that it's just about right. This week's was a bit more than last week's and this amount of work was doable.

3. Is the format of the video tutorials working?
They have been very effective in getting the work done so far and hence I would say so.

4. Are the meetings meaningful?
Yes, having these meetings is useful when some clarifying certain ideas. If not, at least it's a good check-up to know if students are on the right track.

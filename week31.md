Q.1 What did we do?
First, we checked our previous code for Week 29 to make sure that we were on the right track and used efficient computing methods to produce our simulation. Then, we decided to add a recovery period to our simulation. We did this using strings instead of True and False statements to differentiate between sick, healthy and recovered individuals. This meant adding a recovery time to the individual after getting infected.

Q.2 What did I learn?
I learnt about the .format attribute which meant adding one less text command.

Q.3 What questions do I have?
I was wondering if we could test limited movement from the initial position of all the individuals and its effect on the spread of the virus.

```.py
x = [100]
y = [100]
people = 20
count = 0
infected = 0
h = ["Healthy","Sick","Recovered"]
moving = people + 1
days = [30, -1]

def bargraph():
    global infected, x, moving
    line(0,500,500,500)
    healthy = len(x) - infected
    fill(255)
    rect(150, 520, 10*healthy, 20)
    fill(0)
    text("People moving: {}".format(moving), 300, 550)
    text("Healthy {}".format(healthy), 40, 540)
    text
    fill(255,0,0)
    rect(150, 550, 10*infected, 20)
    text("Infected {}".format(infected), 40, 570)

def setup():
    global people, infected, healthy
    size(500,600)
    for n in range(people):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append("Healthy")
        days.append(h)

def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c

def draw():
    global x, people, h, y, count, infected, moving
    background(255)
    infected = 0
    for i in range(len(h)):
        if h[i] == "Sick":
            infected += 1
    bargraph()
    
    for ind in range(len(x)):
        if h[ind] == "Healthy":
            fill(255)
        elif h[ind] == "Recovered":
            fill(0,0,255)
        else:
            fill(255,0,0)
        circle(x[ind], y[ind], 40)
        for nei in range(len(x)):
            if nei == ind:
                continue
            d = distance(x[ind], x[nei], y[ind], y[nei])
            if d < 40 and (h[nei] == "Sick" or h[ind] == "Sick"):
                h[ind] = "Sick"
                h[nei] = "Sick"
                days[ind] = int(random(20, 50))
        if h[ind] == "Sick":
            days[ind] -= 1
            if days[ind] == 0:
                h[ind] = "Recovered"
    for m in range(moving):
        x[m] += random(-20, 20)
        y[m] += random(-20, 20)
        if x[m] > 480:
            x[m] = 480
        elif x[m] < 20:
            x[m] = 20
        elif y[m] > 480:
            y[m] = 480
        elif y[m] < 20:
            y[m] = 20
    count += 1
    textSize(20)
    fill(0)
    text("Run: ", 400, 20)
    text(count, 450, 20)
    delay(50)
```

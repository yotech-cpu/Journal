Q.1 What did we do?

In our lesson on the 4th of March (Tuesday), we were introduced to a software known as "Processing" which I was previously unfamiliar with. Upon talking to some seniors after class however, I managed to learn the usefullness of this software in the future. We immediately switched the language used for programming from Java to Python due to Python's vast versitility in the world of programming. This class, we based our programs on circles. We practiced varying circle sizes, generating circles in random locations, adding text into these circles and changing it's colour to name but a few things. It was extremely fun to get to experiment with this knowledge and apply it to produce some programs. Our first program (given below) consisted of having a circle with a line connected to the middle of the output display wherever we clicked on the screen. In order to test our knowledge, we were given a challenge task of adding lines which joint from circle to circle.

```.java
size (500, 500);
circle (50, 50, 50);
circle (100, 50, 50);
circle (150, 50, 50);
circle (100, 100, 50);
circle (50,100, 50);
circle (100, 150, 50);
```
Last week's code in Java

```.py
def setup():
    size(1000, 1000)
    background(255)
    textAlign(CENTER, CENTER)

def draw():
    print("")
    textAlign(CENTER, CENTER)

def mouseClicked():
    x = mouseX
    y = mouseY
    r = random (0, 255)
    g = random (0, 255)
    b = random (0, 255)
    s = random (10, 40)
    fill (r, g, b)
    line(x, y, 500, 500)
    circle (x, y, s)
    fill(0)
    textSize(s/3);
    text ("Y*Y", x, y)
```
Q.2 What did I learn?

I understood that within the same framework of python, coding could differ significantly however, the knowledge of flowcharts as a base always remains useful. Previously, I was unaware of the usefullness of the global command until I had to complete the homework assignment.

Q.3 What questions do I have?

How do I replicate this with other, more complex shapes?
How can I use this simple knowledge into real-life problem-solving?

```.py
x2 = 0
y2 = 0
x = 0
y = 0

def setup():
    size(1000, 1000)
    background(255)
    textAlign(CENTER, CENTER)

def draw():
    print("")
    textAlign(CENTER, CENTER)

def mouseClicked():
    global x2, y2, x, y
    x2 = x
    y2 = y
    x = mouseX
    y = mouseY
    r = random (0, 255)
    g = random (0, 255)
    b = random (0, 255)
    s = random (10, 40)
    fill (r, g, b)
    line(x, y, x2, y2)
    circle (x, y, s)
    fill(0)
    textSize(s/3);
    text ("Y*Y", x, y)
```
Given above is the code I used to complete the challenge of connect circles with lines. I realized that keeping x,y,x2 and y2 within the def doesn't work as it goes against the flowchart created and x = x2 and y = y2 in that case. However, by using global we solve this issue as the previous variable can be stored.

Thank you!!!

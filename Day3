Q.1 What did we do?

In our lesson on the 18th of February (Tuesday), we were introduced to rectangles in Processing python. We further learnt how to curve the edges of the rectangles with a custom radius for the curve to get rounded rectangles. Then with the use of if statements, our past knowledge on generating random numbers and our knowledge in circles (for a grid), to produce an  unbiased random dice generator. After that, we made the dice biased to a particular number and had a fun acitivity of testing whether we could notice which number was biased.

```.py
def setup():
    size (600, 600)
    background (255)

def draw():
    x = 0
    #circle(200, 200, 50) # top left
    #circle(200, 300, 50) # mid left
    #circle(200, 400, 50) # bot left
    #circle(300, 300, 50) # mid cent
    #circle(400, 200, 50) # top righ
    #circle(400, 300, 50) # mid righ
    #circle(400, 400, 50) # bot righ
    
def mouseClicked():
    stroke(0)
    strokeWeight(10)
    rect(100, 100, 400, 400, 50)
    stroke(255, 0 , 0) #r,g,b
    strokeWeight (10)
    n = random(0, 7)
    
    if 0<=n<1:
        # number one
        circle(300, 300, 50)
    elif 1<=n<2:
        # number two
        circle(200, 200, 50)
        circle(400, 400, 50)
    elif 2<=n<3:
        # number three
        circle(200, 200, 50)
        circle(300, 300, 50)
        circle(400, 400, 50)
    elif 3<=n<5:
        # number four
        circle(200, 200, 50)
        circle(400, 200, 50)
        circle(200, 400, 50)
        circle(400, 400, 50)
    elif 5<=n<6:
        # number five
        circle(200, 200, 50)
        circle(400, 200, 50)
        circle(200, 400, 50)
        circle(400, 400, 50)
        circle(300, 300, 50)
    elif 6<=n<7:
        # number six
        circle(200, 200, 50) # top left
        circle(200, 300, 50) # mid left
        circle(200, 400, 50) # bot left
        circle(400, 200, 50) # top righ
        circle(400, 300, 50) # mid righ
        circle(400, 400, 50) # bot righ
    else:
        print ("Way to cheat the system ma man")
```
Code for the program we made done in class (biased dice) ^
Can you guess which number the die favours?

Q.2 What did I learn?

I learnt how rectangles are produced in Processing python and how to get rounded edges on them. More importantly, I learnt how programs don't really require complex code. They can be made from the most basic of concepts that we may already be aware of.

Q.3 What question do I have?

How does the random function work within? Can it really just randomly generate a number? What is the algorithm behind it?

Homework

Adding a probability bar graph to the dice with a roll counter.

```.py
rolls = 0
oney = 500
twoy = 500
threey = 500
foury = 500
fivey = 500
sixy = 500
def setup():
    size (600, 600)
    background (255)

def draw():
    global rolls, pre_rolls, oney, twoy, threey, foury, fivey, sixy
    background (255)
    fill(255)
    stroke(0)
    strokeWeight(10)
    rect(150, 100, 400, 400, 50)
    stroke(255, 0 , 0) #r,g,b
    strokeWeight (10)
    n = random(0, 6)
    
    if 0<=n<1:
        # number one
        circle(350, 300, 50)
        oney -= 1
        text ('1', 10 ,550)
        line(20, 500, 20, oney);
    elif 1<=n<2:
        # number two
        circle(250, 200, 50)
        circle(450, 400, 50)
        twoy -= 1
        text ('2', 30 ,550)
        line(40, 500, 40, twoy);
    elif 2<=n<3:
        # number three
        circle(250, 200, 50)
        circle(350, 300, 50)
        circle(450, 400, 50)
        threey -= 1
        text ('3', 50 ,550)
        line(60, 500, 60, threey);
    elif 3<=n<4:
        # number four
        circle(250, 200, 50)
        circle(450, 200, 50)
        circle(250, 400, 50)
        circle(450, 400, 50)
        foury -= 1
        text ('4', 70 ,550)
        line(80, 500, 80, foury);
    elif 4<=n<5:
        # number five
        circle(250, 200, 50)
        circle(450, 200, 50)
        circle(250, 400, 50)
        circle(450, 400, 50)
        circle(350, 300, 50)
        fivey -= 1
        text ('5', 90 ,550)
        line(100, 500, 100, fivey);
    elif 5<=n<6:
        # number six
        circle(250, 200, 50) # top left
        circle(250, 300, 50) # mid left
        circle(250, 400, 50) # bot left
        circle(450, 200, 50) # top righ
        circle(450, 300, 50) # mid righ
        circle(450, 400, 50) # bot righ
        sixy -= 1
        text ('6', 110 ,550)
        line(120, 500, 120, sixy);
    else:
        print ("Way to cheat the system ma man")
    rolls += 1
    fill(0)
    textSize(40)
    text ('Rolls: ', 350, 550)
    text (rolls, 460, 550)
    delay(10);
    text ('1', 10 ,550)
    line(20, 500, 20, oney);
    text ('2', 30 ,550)
    line(40, 500, 40, twoy);
    text ('3', 50 ,550)
    line(60, 500, 60, threey);
    text ('4', 70 ,550)
    line(80, 500, 80, foury);
    text ('5', 90 ,550)
    line(100, 500, 100, fivey);
    text ('6', 110 ,550)
    line(120, 500, 120, sixy);
    textSize(20)
    text ('Finish line!!!', 15, 20)
    stroke (0)
    strokeWeight(2)
    line (10, 30, 140, 30)
```

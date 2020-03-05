Q.1 What did we do?

We were told to look at two videos on Generative Art and Game Boards respectively. I decided to make two programs based on these ideas.

Q.2 What did I learn?

I learnt about the round function to lock the chess piece in the center of each square on the chessboard.

Q.3 What questions do I have?

How can I limit the moves of actual chess pieces and display the valid moves for them?

Below is the code for a canvas that paints itself:
```.py
def setup():
    size(500, 500)
    background(255)

def draw():
    r = random(0, 255)
    g = random(0, 255)
    b = random(0, 255)
    x = random(4, 495)
    y = random(4, 495)
    randomize = random(20, 40)
    for i in range (5):
        noStroke()
        plus_minus = random (0,4)
        one = random(5, 50)
        two = random(5, 50)
        three = random(5, 50)
        four = random(5, 50)
        s = random (50, 100)
        fill (r, g, b)
        circle (x, y, s)
        if 0 <= plus_minus < 1:
            x += randomize
            y += randomize
        if 1 <= plus_minus < 2:
            x -= randomize
            y += randomize
        if 2 <= plus_minus < 3:
            x += randomize
            y -= randomize
        if 3 <= plus_minus < 4:
            x -= randomize
            y -= randomize
    delay(100)
    fill(0)
```

Below is the code for a chess piece that has unlocked hacks on the chessboard and can move to any block:
```.py
c = 350
d = 750
def setup():
    size(800, 800)
    background(255)
    textAlign(CENTER, CENTER)
def draw():
    global c, d
    stroke(0)
    y = 0
    for n in range(8):
        line(0, y, 500, y)
        y += 100
    fill(0)
    stroke(255)
    y = 0
    for n in range(5):
        x = 0
        for n in range(5):
            square(x, y, 100)
            x += 200
        y += 200
    # odd rows
    y = 100
    for n in range(5):
        x = 100
        for n in range(5):
            square(x, y, 100)
            x += 200
        y += 200
    fill(255, 0, 0)
    circle (c, d, 80)
    fill(0)
    textAlign(CENTER, CENTER)
    textSize(80/4);
    text ("Hacks", c, d)
def mouseClicked():
    global c, d
    background(255)
    c = mouseX
    d = mouseY
    c = c // 100
    d = d // 100
    c = round(c)
    d = round(d)
    noStroke()
    c = (c * 100) + 50
    d = (d * 100) + 50
    circle (c, d, 80)
    fill(0)
    textAlign(CENTER, CENTER)
    textSize(80/4);
    text ("Hacks", c, d)
```

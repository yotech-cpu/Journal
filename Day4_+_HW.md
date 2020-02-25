Q.1 What did we do?

In our fourth class on Processing on the 25th of February, we briefly went over our previous homework of adding a roll count and bar graphs to our die. Then, we went straight into optical illusions by creating one together in class. This one consisted of a checkers board being offset every alternate line by a certain value every time we clicked on it. This gave us the illusion of diagnol lines while in reality they were still parallel. Needless to say, I lost any sense of reality I once had.

Q.2 What did I learn?

I learnt about the for loop in python and its general uses. I was surprised by how we managed to make some solid programs with really simple knowledge of python.

```.py
offset = 50
def mouseClicked():
    global offset
    offset += 1
def setup():
    size(500, 500)
    background(255)
def draw():
    stroke(0)
    y = 0
    for n in range(10):
        line(0, y, 500, y)
        y += 50
    fill(0)
    stroke(255)
    y = 0
    for n in range(5):
        x = 0
        for n in range(5):
            square(x, y, 50)
            x += 100
        y += 100
    # odd rows
    y = 50
    global offset
    for n in range(5):
        x = 0 + offset
        for n in range(5):
            square(x, y, 50)
            x += 100
        y += 100
```

Q.3 What questions do I have?

Regarding the homework, I was wondering what I could do to make the lines disapper on click even while holding down on the button.

Here's the optical illusion I recreated:

```.py
counter = 0
blockWidth = 44;
blockHeight = 20;
stripWidth = 11;
yYellow = 40;
yBlue = 130;
jai = 0
def setup():
    size(484, 200)
    background(255)

def mouseDragged():
    global counter, stripWidth, blockWidth, blockHeight
    background(255)
    strokeWeight (0)
    fill(255,255,0);
    rect(counter, yYellow, blockWidth, blockHeight);
    # draw yellow rectangle
    fill(0,0,255);
    rect(counter, yBlue, blockWidth, blockHeight);
    # after leaving the canvas restart at left
    if (counter == 484):
        counter = 0

def draw():
    global counter, stripWidth, blockWidth, blockHeight, yYellow, yBlue, jai
    background(255)
    if (jai < 174):
        jai = jai+(2*11)
        fill(0)
        rect(jai, 0, stripWidth, 174)
    x = 5
    stroke = 11
    for n in range (30):
        strokeWeight (11)
        line (x, 0, x, 174)
        x += 22
    # draw yellow rectangle
    counter += 1
    strokeWeight (0)
    fill(255,255,0);
    strokeWeight (11)
    line (0, 174, 484, 174)
    strokeWeight (0)
    rect(counter, yYellow, blockWidth, blockHeight);
    # draw yellow rectangle
    fill(0,0,255);
    rect(counter, yBlue, blockWidth, blockHeight);
    # after leaving the canvas restart at left
    if (counter == 484):
        counter = 0
    fill (0)
    text ("* Please switch between continously dragging around your mouse and not", 10, 190)
```

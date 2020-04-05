Inquiry question: What strategy is the most efficient to contain the spread of a virus in a general population?

Q.1 What did we do?
We read through the article "How your personal computer can help science battle the coronavirus while you sleep"　by John D'Anna for Arizona Republic Magazine, 

Q.2 What did I learn?
I learnt that I can actually contribute to finding the cure to the coronavirus in simpler way than I had previously imagined. I also learnt about the append method which came in handy for the coding task.

Q.3 What questions do I have?
How close can this simulation get to the real-world scenario?
What is the most effective method?

Q.4 What are some ways in which Computer Science can help the fight against Covid-19?
With the help of a networked "super-cluster" of volunteers, scientists can get volunteers from around the world to gain the computer power required to run simulations, etc. This means that gamers, or anyone really with a computer can put their computer to use while idle in order to contribute to the cause. Additionally, machine learning can be used to find Covid-19 drugs.

Q.5 In your opinion, should people enable access to the resources of their personal computers as tools for research? Are there any risks?
I believe that in such times, such efforts show how the world can get together despite our differences; whether we're a gamer with a solid gaming rig or a nucleur power station that is idle. This is a great display of how the world is together. However, there are certain individuals and organisations who may take advantage of such vulnerable moments in order to find easy means of hacking into computer systems around the world which could make our data at severe risk.

Q.6 What should be some behaviours (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain.
A difference in sanity (washing hands for example) should be included in our simulation as it affects the contraction of our disease. Moreover, we should check if limiting each person's movement to a certain radius actually helps limit the spread of the disease or just slows down the speed at which the virus is spread. In addition to this, implementing social distancing would also be something that should be tested as a behaviour. People tested positive should also be moved out into a quarantine zone to recover.

```.py
number_of_people = 10
x = []
y = []
for xc in range (number_of_people):
    x.append(random(501))
for yc in range (number_of_people):
    y.append(random(501))

def setup():
    size(500,500)
    
def draw():
    global x, y, number_of_people
    background(255)
    strokeWeight(2)
    
    for i in range(number_of_people):
        print x, y
        circle(x[i], y[i], 40)
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)
        
        if x[i] > 500:
            x[i] = 500
        elif x[i] < 0:
            x[i] = 0
        elif y[i] > 500:
            y[i] = 500
        elif y[i] < 0:
            y[i] = 0
    
    delay(100)
 ```

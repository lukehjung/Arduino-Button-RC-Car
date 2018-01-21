# Arduino Button RC Car
This is an Arduino Tutorial for creating a remote controlled wheel robot.  Created (6/2/16) for Mr Robinette's Comp Sci Class.

Tutorial for Creating Arduino Button Controlled Car.
By Luke Jung, William Guan, and Andrew Rim
Materials
•    Old RC car taken apart
•    AA batteries
•    Arduino starter kit
•    Computer/laptop to code Arduino
•    Videos/Forums/Threads to learn code and get ideas for projects
Tutorial

Review Java Concepts
Class
Object
Boolean
If statements
Instance Variables

Study for Arduino
setup()
pinMode()
digitalRead()
delay()
loop()
LOW/HIGH

Step 1: Getting Started
So to begin with Arduino, we need to understand what an Arduino is.  Arduino is a type of computing chip that takes input for building various digital devices and interactive objects using circuits and wires.
To start, we recommend spending a lot of time researching how the Arduino works with learning the different methods talked about above.  Also, research how switches work, what breadboards are, the different ways you can harm your Arduino unit, shields, relays, and jumper cables, and resistors.
Once you understand the following parts and how they work, obtain the following and we can start building the board.
•    6 M/M Jumper cables
•    2 M/F Jumper cables
•    1 Relay
•    1 220 ohm resistor
•    1 mini switch button
•    Pair of rc wheels/motors
•    1 battery pack
•    3 hair ties/tape


Step 2: Setting up the Relay
The first step to setting up our circuit board is to attach the Arduino shield with mini breadboard on top.  To attach the mini breadboard, simply take off the covering from the adhesive and stick in on top a shield (it doesn’t have to be exactly on a certain circuit, just keeps it on there).
So the first part we want to do is set up the relay.  If you researched, a relay is an electro-magnetic switch that can use a relatively small current to power a much larger resistor like the wheels we want.
So set up the relay on the left side of the board like so.

![pic_1](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/1.png?raw=true)
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/2.png?raw=true)

•    We want to the red wire to relay number 1 to the green 3 on the top side
•    The blue wire from relay 2 to the red ground below it
•    The black wire from relay 4 to ground in the black

Step 3: Setting up the Switch
Now we need to set up the switch.  So a switch does exactly what it seems it would do.  It gives a response to the board to the energy it’s experiencing.  It has two modes, High and Low, and when we use a digital read on the switch, we can tell whether or not to put power through the relay and therefore the wheels.
So set up the switch on the right side of the board like so
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/3.png?raw=true)
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/4.png?raw=true)

•    Connect the white wire from position 2 to the 5V at the red side on the right
•    Connect your 220 ohm resistor from position 1 to 3 steps away to the left side
•    Connect the green wire from right above the resistor’s left side to the Gnd in the above green row
•    Connect the red wire from the right side of the resistor to 2 on the green row above

Step 4: Connect the Wheels
Now for the last step, we just need to connect the rc car wheels. Usually, these wires are in a strand, so it’s hard to connect them to our breadboard or other parts of our shield.  Therefore we use the F/M jumper cables to extend the wires and make it easier to plug in.
For these, we plug it in like the following.
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/5.png?raw=true)
•    Connect the blue jumper cable to position 6 of the relay
•    Connect the white jumper cable to the bottom most slot of the red row on the right
And that’s it for the Board!! Now we can finally go onto the programming part.
Step 5: Writing the Program
So the first thing we want to do write in our program are the instance variables we want to use.  The code we wrote included these
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/6.png?raw=true)
The next method we use is to setup the board, which is just setting up input or output
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/7.png?raw=true)
The next method we need is the debounce method.  Debounce is a method used to make sure the button works as wanted.  Since the switch is made with the connection of metal hitting each other.  Sometimes the button doesn’t depress right and the program doesn’t know whether or not to change the current to the relay.  Therefore we can create a method to wait 5 ms before reading so that it gives the button time to bounce and get the correct information.
Therefore our code looks like so
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos/8.png?raw=true)
The next method we use is the loop which is the main part of how our program continues to run.
![alt text](https://github.com/lukejung99/Arduino-Button-RC-Car/blob/master/Photos9.png?raw=true)
And that’s the code!
Compile it using the check at the top to make sure the code runs, then making sure you disconnect the wheels first so it doesn’t take all the energy from your laptop, send the code to the Arduino and let it sync up!
Step 6: Attaching the Board and Power Supply to the Wheels
Now that all the components are done, we just need to attach them together.  Using the battery pack from the kit, put 6 AA batteries in and connect it to the board.  Attaching the supply and board is up to you on how you want to, but make sure it’s secure.  Once that’s done, every time you push the button it should turn the wheels on and off.
That’s it.  If you have any other questions contact us!  Happy driving.


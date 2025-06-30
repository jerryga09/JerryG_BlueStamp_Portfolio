# Gesture Controlled Robot
The Gesture Controlled Robot is operated from a gauntlet device someone can wear on their wrist. By tilting or rotating the wrist, users can move the robot in all sorts of directions.

<!---You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Jerry G | Lynbrook High School | Mechanical Engineering | Incoming Sophomore

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.** -->

![Headstone Image](logo.svg)
  
# Final Milestone

<!--- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!--- <iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->

<!--- For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE -->



# Second Milestone

<!--- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!--- <iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->
My second milestone was mostly about bluetooth. First off, I had to connect and pair the two HC05's. I searched up many tutorials about how to do this. The process included going into AT Mode, changing the settings of the Master & Slave HC05's, etc. One main challenge that I encountered was trying to figure out how to use a voltage divider. Because my arduino nano runs on 5V and the HC05 uses 3.3V, I had to use a voltage divider to make sure the HC05 doesn't get damaged. I spent at least half a day trying to figure this out, until I realized that I had an accelerometer to use (because of this I didn't use a voltage divider). I was able to get the accelerometer to print out data in the form of acceleration in the x, y, and z directions, as well as the acceleration of the rotation in the x, y, z directions. The final part of this milestone was to send the data from the accelerometer to the arduino uno. This was arguably the hardest part of the milestone and it definitely took a lot of time, but I was able to accomplish this in the end. 
For my final milestone, my goal is to put everything together. Most of it will be writing code to turn the accelerometer data into actual movements of the robot. 

<!--- For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

# First Milestone

<!--- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<iframe width="560" height="315" src="https://www.youtube.com/embed/7Dbkg9NT-sA?si=TJ2dOaJaLXVbonkF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> 

My first milestone was essentially building the hardware section of the robot. I assembled the car and attached all the motors. I soldered wires onto the motors and made sure the motors were locked into place on the chassis. Important materials that I used during milestone 1 included 2 L298 motor drivers, an Arduino Uno R3, a breadboard, 4 DC motors, and the chassis. I wired everything and connected all the pins with the help of a breadboard. The motor drivers received commands such as HIGH or LOW, HIGH meant the motor should spin, LOW meant it shouldn't. After writing some simple code just to make sure the motors would spin, I uploaded the code to the Arduino Uno, which is responsible for processing commands. Now, all I needed to do was to power it all up using a 9V battery that was connected to a barrel jack wire. I ran the code, and all 4 motors were able to work. So far, everything has gone smoothly. I had some problems understanding how to assemble the chassis and I had to de-assemble the top because I forgot to solder wires onto the motors, but all I had to do was unscrew the top. My biggest concern right now is the organization. The motor drivers, breadboard, and arduino are all currently just sitting on top of the actual robot, so there are a lot of wires just floating around which is really confusing. All the components aren't set yet, but I plan on zip tying everything down once I make sure that's where I want everything. Next, I plan on moving to milestone 2, which is starting the bluetooth section. This includes creating the actual gaunlet someone will be wearing, using the bluetooth modules, and wiring everything together. 

Figure :Overhead Picture of Completed Milestone 1

<img src="IMG_2859.jpg" alt="Headstone Image" width="400">

### Code for motors

```
int motor1pin1 = 2; 
int motor1pin2 = 3;


int motor2pin1 = 4;
int motor2pin2 = 5;


int motor3pin1 = 8;
int motor3pin2 = 9;


int motor4pin1 = 10;
int motor4pin2 = 11;


void setup() {
 pinMode(motor1pin1, OUTPUT);
 pinMode(motor1pin2, OUTPUT);
 pinMode(motor2pin1, OUTPUT);
 pinMode(motor2pin2, OUTPUT);
 pinMode(motor3pin1, OUTPUT);
 pinMode(motor3pin2, OUTPUT);
 pinMode(motor4pin1, OUTPUT);
 pinMode(motor4pin2, OUTPUT);

//code for all motors to spin in the same direction

 digitalWrite(motor1pin1, LOW);
 digitalWrite(motor1pin2, HIGH);
 digitalWrite(motor2pin1, LOW);
 digitalWrite(motor2pin2, HIGH);
 digitalWrite(motor3pin1, LOW);
 digitalWrite(motor3pin2, HIGH);
 digitalWrite(motor4pin1, LOW);
 digitalWrite(motor4pin2, HIGH);

 delay(5000); //spin for 5 seconds

 digitalWrite(motor1pin1, LOW);
 digitalWrite(motor1pin2, LOW);
 digitalWrite(motor2pin1, LOW);
 digitalWrite(motor2pin2, LOW);
 digitalWrite(motor3pin1, LOW);
 digitalWrite(motor3pin2, LOW);
 digitalWrite(motor4pin1, LOW);
 digitalWrite(motor4pin2, LOW); //code to stop motors
}
```

<!--- For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project -->

# Schematics 
<!--- Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. -->
Figure :Schematic of Milestone 1

<img src="mileston1circuit.png" alt="Headstone Image" width="400">

# Code
<!--- Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. -->
<!---
```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```
-->
# Bill of Materials
<!--- Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. -->
<!---
| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> | -->

<!--- # Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here. -->

# Starter Project - 6/17/25

<iframe width="560" height="315" src="https://www.youtube.com/embed/2kwSJgJjW6E?si=UGgxnVTeYXJCwrKC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Summary
For the starter project, I chose the RGB Slider. The RGB Slider features three sliders, one that corresponds for the Red, Green, and Blue values of an LED light. It is powered through a USB-C port. Finally, there's the LED light that ultimately displays the colors. This project also allows for colors to mix (when the red and blue sliders are slid to the maximum, purple light is shown). 
### Challenges
Although this project was straightforward, I encountered challenges while working on this project. The first challenge I met was after I had soldered on all the components. I plugged the power in and played around with the sliders, but the LED light wouldn't turn on. I asked my instructor and it turns out that I had soldered the LED light on the wrong way. So I had to de-solder the LED light using a desoldering pump. After this was finished, I tested with the power on again. The red and blue sliders worked perfectly, but the green slider didn't work at all. My instructor thought that the plastic board had been faulty, so I restarted from scratch. After doing the entire process again, all three sliders finally worked, resulting in an exciting RGB Slider starter project. 
### Next Steps
Next, I will be starting my intensive project, which is the Gesture Controlled Robot. 

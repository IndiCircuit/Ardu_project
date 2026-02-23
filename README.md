# Blink a LED 
Hello! In this project, we want to blink an LED. It is where it all starts, a perfect project for the beginners, so stay with me for some time and let's get into it!

# Materials


In this project, you will need :
- An Arduino board (Can be any of them, or even other similar brands like Elegoo but that are compatible with Arduino IDE)
- A breadboard 
- 2 Cables
- A resistance of 100 Ohms
- An LED {of your favourite colour if possible ;) }
- A cable that is able to connect the Arduino board to your computer
- A twinky little bit of time :)

Here are some photos of the elements I am using for this project : 

<img src="https://github.com/user-attachments/assets/1738f91c-a8dc-477e-8b9e-f268b63e07e5" width="250" > - This is the Elegoo Uno R3 that I use as Arudino Board (highly recommend buying boards from them it's so much cheaper yet adapted for projects and as powerful)


<img src = "https://github.com/user-attachments/assets/9f579c6a-15e6-4685-8820-7dfad6f3d4d5" width="300" >- The 100 Ohms resistance that I use for this project (If you don't know how much Ohms yours is, check the colors and compare with a reference pic {could be my image or one from the Internet for example})


<img src = "https://github.com/user-attachments/assets/cba4d5c5-f7a0-451b-8e89-7da0974d3abf" width="300" rotate="90"> - Those are called I think male to male cables, it can be squarish at the end (the black part) or round, it doesn't really matter the form of it, they just need to both have that same end as shown in the picture (the grey wire itself)


<img src = "https://github.com/user-attachments/assets/aa6b7dfa-429a-4a3e-9cc9-0bb64d89b854" width = "300" >- This is an LED, a green one since it's my favourite colour :) 


<img src="https://github.com/user-attachments/assets/e68eabb6-18d5-45a4-a651-37e2610f22fb" width = "300">  - This is the cable that I use to connect my board to my computer. It is very important to make sure it is in a good state, so that a proper connection between the board and the computer is made. 


<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/54456e3f-9776-4db6-8eb6-36be10b0f1e5" /> - This is my breadboard! As you noticed, it has red and blue strips that seperate two parts (one in the right and one in the left). Well those parts are called buses. For now, we don't really need them but later they help a lot, you'll see! (But remember, the size of the breadboard doesn't really matter, if you just have enough space to work!)


Now that we have the materials we need to blink an LED, let's start wiring and connecting things up! Don't worry, I will be with you during the whole process with some images for each step, so that you don't miss anything! 

# Connections


## Step 1 : 
Put the LED somewhere in your breadboard. Make sure that you notice where the longer leg is and where the smaller leg is! Usually, the longer is positive (we call it Anode) and the shorter leg is negative (we call it cathode)! 

## Step 2 : 
Connect the resistance to the LED to the anode of the LED just like in the picture. 

## Step 3 : 
Connect the other end of the resistance with a cable to any digital pin of your board (those from 13 to 0). 

## Step 4 : 
Connect the other cathode of the LED to the ground.

## Step 5 : 
Check if your circuit is well connected. It is the most important step in every Arduino project or just anything! Making sure of it saves your electronic pieces, trust me!

## Step 6 : 
The final step of connections, connect the board to you computer. Now that everything is well connected and that no short-circuit can happen, You can finally give instructions to your board, the brain of the circuit!

# Code

If you had some experience in coding languages such as python or any other, understanding this code will be faster for you than for anyone else! But even without knowing the basics of coding, it doesn't mean that you will get completely lost! Let's get into it! 

Here is the code : (in the Arduino IDE of course! If you prefer instead of copying-pasting it to download it, check my file 'Blinky.ino'!)

```
void setup() {
  pinMode(13, OUTPUT) ;
} 

void loop() {
  digitalWrite(13,HIGH)
  delay(1000);
  digitalWrite(13,LOW)
  delay(1000);
} 
```
# Explanation of the code

## FOR THE VOID SETUP : 

As you saw before, we connected our LED/resistance to the digital entry of our breadboard 13. The void setup function is the one that runs once when the code is activated. Usually, in this function we initiate variables, specify whether the pin is an output or an input (using the pinMode that we did, in which pinMode(number of the pin, OUTPUT or INPUT), and do many other interesting stuffs. If you didn't know, an output controls actuators (LED, dc motors, etc...) , while an input read signals (buttons, potentiometer, sensors, etc...). For outputs, we connect them to the digital pins, while for the iputs we connect them to the analog pins (we'll use an input in our next project!) In our case, our LED is connected to the pin 13 (we don't count the resistance here), and an LED is an OUTPUT, that's why we said in the void setup : pinMode(13,OUPUT). 

## FOR THE VOID LOOP 

The void loop function is the one that runs forever when the code is activated. In this function, we perform actions such as reading the sensors or control the outputs, or even setting some conditions and many other fun stuffs. In ours, we see the command digitalWrite(). This command literally tells our LED what it needs to do. In the parenthesis of the command, we see (13,HIGH) which literally translates to : for the microcontroller connected to the pin 13, be on (which is in it HIGH). The same thing happens after with the digitalWrite(13,LOW), but instead of telling our LED to be on, it tells it to be off(which is in it LOW). Now if you saw it, there is between a delay command. This command is what makes the LED blink. Lemme explain more clearly. When the LED is on with the digitalWrite(13,HIGH) command, it waits a second with the delay(1000) command. It literally tells our LED : Okay, stay on for a second, like wait for a second. And then, after waiting a second, it can be off with the digitalWrite(13,LOW) command, and wait again with the delay(1000) after it. Try to remove if you want the delay(1000) and see what happens :). 

# Little Challenges :) 

Electronics are really fun when there are challenges that makes your brain reflect a little harder. Here are some that will determine whether you understood or not!
-  Challenge 1 : Make the LED blink faster;
 <details>
  <summary>See solution 1</summary>
   
```
  digitalWrite(13,HIGH)
  delay(200);
  digitalWrite(13,LOW)
  delay(200);
```
(it can be any number in it, if at least smaller than 1000) 
</details>

-  Challenge 2 : Make the LED blink slower ;
<details>
  <summary>See solution 2</summary>

  ```
  digitalWrite(13,HIGH)
  delay(1200);
  digitalWrite(13,LOW)
  delay(1200);
```
(it can be any number, if at least greater than 1000)
</details>

-  Challenge 3 : Make the LED be more off than on ;
<details>
  <summary>See solution 3</summary>
  
````
  digitalWrite(13,HIGH)
  delay(200);
  digitalWrite(13,LOW)
  delay(800);
````
(can be any number if it follows the same logic, more time in LOW than in HIGH)
</details>

-  Challenge 4 : Make the LED more on than off ;
<details>
  <summary>See solution 4</summary>

````
  digitalWrite(13,HIGH)
  delay(800);
  digitalWrite(13,LOW)
  delay(200);
````
(can be any number if it follows the same logic, more time in HIGH than in LOW)
</details>

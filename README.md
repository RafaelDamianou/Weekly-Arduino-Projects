# Weekly-Arduino-Projects
# 3-LED Traffic Light

## Overview
This project simulates a **traffic light system** using an **Arduino Uno** and three LEDs — **red, yellow, and green**.  
It demonstrates basic digital output control, timing using delays, and sequential logic, making it an ideal beginner project for learning Arduino fundamentals.

---

## Components

| Component | Quantity | Description |
|------------|-----------|-------------|
| Arduino Uno | 1 | Microcontroller board 
| Red LED | 1 | Stop light |
| Yellow LED | 1 | Wait / caution light 
| Green LED | 1 | Go light 
| 220Ω Resistors | 3 | Current limiting resistors 
| Breadboard | 1 | For easy prototyping 
| Jumper Wires | Several | For connections 

---

## Circuit Connections

| LED Color | Arduino Pin | Description |
|------------|--------------|--------------|
| Red LED | Pin 13 | Stop signal 
| Yellow LED | Pin 12 | Warning signal 
| Green LED | Pin 11 | Go signal 
| All LEDs | GND | connected to ground 

###Connection Steps
1. Connect each LED to its respective Arduino pin through a **220Ω resistor**.  
2. Connect all of the LEDs to the **GND** pin on the Arduino Uno.  

---

## Arduino Code

```cpp
// 3-LED Traffic Light for Arduino Uno
// Red -> 13, Yellow -> 12, Green -> 11

int redLED = 13;
int yellowLED = 12;
int greenLED = 11;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(yellowLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
}

void loop() {
  // Green light ON for 5 seconds
  digitalWrite(greenLED, HIGH);
  delay(5000);
  digitalWrite(greenLED, LOW);

  // Yellow light ON for 2 seconds
  digitalWrite(yellowLED, HIGH);
  delay(2000);
  digitalWrite(yellowLED, LOW);

  // Red light ON for 5 seconds
  digitalWrite(redLED, HIGH);
  delay(5000);
  digitalWrite(redLED, LOW);
}

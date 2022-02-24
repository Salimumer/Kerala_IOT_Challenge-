# Kerala_IOT_Challenge-
Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation



# About Me
Hello friends! My name is SALIM UMER and Currently pursuing diploma in Electrical and Electronics Engineering at government polytechnic college perinthalmanna. my area of interest is mainly on iot and cyber security. I used to do small projects using Arduino

# Experiment 1 : Hello World LED Blinking
A basic program similar to printing "Hello World" in any programming language. The aim is to blink an LED using Arduino Uno Board. Currently I am using tinkercad an online stimulator for doing the experiments.

Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

Components Required
- Arduino Uno Board
- LED (Any Color) x 1 Nos
- 220 OHM Resistor X 1 Nos
- Breadboard
- Connecting wires

Code
```
#define LED 8
void setup()
{
  pinMode(LED, OUTPUT);
}

void loop()
{
  digitalWrite(LED, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(LED, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```

# Circuit Diagram 
![exp1](https://user-images.githubusercontent.com/84274432/155352790-3f78d4c6-5f92-4b95-8acc-70ddd34fd084.png)

# Video
![ezgif com-gif-maker](https://user-images.githubusercontent.com/84274432/155355228-3a2c1945-9ff6-4bd1-b27e-c58ccb90a62b.gif)

 
# Experiment 2 : Traffic Light
> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

# Components Required

- Arduino board X 1
- Red LED X 1
- Yellow M5 LED X 1
- Green M5 LED X 1
- 220Ω resistor X 3
- Connecting wires


# Circuit Diagram
![148655120-3609e8f5-ad4a-4433-a2ca-038ed789753a](https://user-images.githubusercontent.com/84274432/155356225-f63044fc-4657-4b37-b5b4-8ebef7324c78.png)

Code
```
#define led1 13
#define led2 12
#define led3 11
void setup()
{
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop()
{
  digitalWrite(led1,HIGH);
  delay(5000);
  digitalWrite(led1,LOW);
  for(int i=0;i<3;i++){
    delay(500);
    digitalWrite(led2,HIGH);
    delay(500);
    digitalWrite(led2,LOW);
    delay(500);
  }
  digitalWrite(led3,HIGH);
  delay(5000);
  digitalWrite(led3,LOW);
  delay(500);
}
```

# video
![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/84274432/155358308-294b8e87-0447-4c3d-befc-aab75ace1039.gif)

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.


# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

# Components Required
- Led X 6
- Arduino board X 1
- 220Ω resistor X 6
- Breadboard X 1
- Connecting wires

# Circuit Diagram

![148656072-3079c4e4-d35c-48d1-9515-521e977dfc3b](https://user-images.githubusercontent.com/84274432/155358792-976702e4-920f-482a-ac07-c3c8b19e5b7a.png)

## Code

```
#define pin 2
#define num 6
void setup()
{
  for(int i=pin;i<pin+num;i++){
   pinMode(i,OUTPUT); 
  }
}

void loop()
{
  for(int i=pin;i<pin+num;i++){
   digitalWrite(i,HIGH);
   delay(200); 
  }
  for(int i=pin;i<pin+num;i++){
   digitalWrite(i,LOW);
   delay(200);
  }
}
```
# Experiment 4 : Button Controlled LED

> An experiment to light an LED using a Push Button.

##  Components Required


- Arduino Uno
- Button switch x 1
- Red M5 LED x 1
- 220ΩResistor x 1
- 10KΩ Resistor x 1
- Breadboard x 1
- Connection wires

# Circuit Diagrams

![148673943-4e88b419-ef66-4436-bfd3-809f56dfd5e3](https://user-images.githubusercontent.com/84274432/155370020-9c392f94-4627-4305-8ce8-7d06badb0ef5.png)

## Code

```
#define led 10
#define button 7
int x;
void setup()
{
  Serial.begin(9600);
  pinMode(led, OUTPUT);
  pinMode(button, INPUT);
}

void loop()
{
  x=digitalRead(button);
  Serial.println(x);
 
  if(x==LOW){
    digitalWrite(led, HIGH);
  }
  else{
    digitalWrite(led, LOW);
  }
}
```

# Output


![148674078-1369d46f-8f98-4c64-bb7b-6f9c8eb29bbf](https://user-images.githubusercontent.com/84274432/155370480-76226424-24b9-40a5-88cf-4e1e3c584844.png)

# Video 
![exp4_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155371646-0744f8b3-cda6-40d4-8195-1088bbb616e1.gif)


# Experiment 5 : Buzzer
> An experiment to understand the working of a buzzer.

## Components Required

- Arduino Uno
- Buzzer x 1
- Breadboard x 1
- Connecting wires

# Circuit Diagrams

![148674078-1369d46f-8f98-4c64-bb7b-6f9c8eb29bbf](https://user-images.githubusercontent.com/84274432/155372434-9aa08b94-d417-4512-b818-8f6a68c66ebd.png)

# Code
```
#define buz 3
void setup()
{
  pinMode(buz, OUTPUT);
}

void loop()
{
  digitalWrite(buz, HIGH);
  delay(1000);
  digitalWrite(buz, LOW);
  delay(1000); 
}

```
# Output

![148674461-7abb33b8-9be7-4b4e-9edb-6a666fd440e9](https://user-images.githubusercontent.com/84274432/155372855-a45276b0-ae39-43c3-bef0-372681281357.png)

# Video

![exp5_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155373786-b620c216-0ee1-4b1e-bff2-84ec9ed22d3d.gif)


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

# Components Required

- Arduino Uno
- USB Cable x 1
- RGB LED x 1
- 220ohm Resistor x 3
- Breadboard jumper wire x 4

# Circuit Diagrams


![137347719-6966c0b1-021d-471c-b0a7-48d0441752d0](https://user-images.githubusercontent.com/84274432/155374320-6208edbc-1b5e-48cb-9e6a-0aec70ecdf0d.png)

![137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72](https://user-images.githubusercontent.com/84274432/155374495-ee6b5ce0-1f92-4d8f-8e02-490bd36a2475.png)

![137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818](https://user-images.githubusercontent.com/84274432/155374552-37046f27-8d55-4fbe-88af-436e2e3bfd61.png)


# Code

```
int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```

# Output
![exp6_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155375634-78c6c8ac-e212-4e56-ae81-3a25d80be30e.gif)

# Experiment 7 : LDR Light Sensor
  
  > An experiment to understand the working of an LDR light Sensor.
## LDR : Light Dependent Sensor

>Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

# LDR


![138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5](https://user-images.githubusercontent.com/84274432/155375934-2975b733-a119-44d5-8527-f75bd89677e0.png)

# Components Required

- Arduino Uno Board
- LDR module x 1
- GREEN LED x 1
- Breadboard x 1
- Breadboard Jumper Wire x 6
- USB cable x 1


# Circuit Diagrams
![151673336-172ff2c3-6b7b-4ab3-af6f-ca861e5b4bb1](https://user-images.githubusercontent.com/84274432/155376150-57f8df19-6eda-4e49-a679-4ea23820e622.png)

# Code
 ```
#define ldr A0
#define led 3
int x;
void setup() {
  pinMode(ldr, INPUT);
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}
void loop() {
  x=analogRead(ldr);
  Serial.println(x);
  if(x>=1000){
    digitalWrite(led,HIGH);
    Serial.println("HIGH");
  }
  else{
    digitalWrite(led,LOW);
    Serial.println("LOW");
  }
  }
 ```
 # Output
 ![exp7_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155376808-e6d9c77b-8a5e-41a1-a328-38aaefd6cc46.gif)

# Experiment 8 : Flame Sensor


> An experiment to understand the working of a flame sensor

 
## Flame Sensor


![151690789-70672b9b-bf4a-4714-8f4c-48bf1995c62d](https://user-images.githubusercontent.com/84274432/155377040-651671d2-c803-46f2-bf38-04073b2cce63.png)


# Components Required

- Arduino Uno
- Flame sensor x 1
- Breadboard x 1
- Jumper wire x 7
- buzzer x 1
- GREEN LED x 1
- RED LED x 1
- 10k Resistor x 1



![151690868-ae0d09fd-c798-42e0-a970-07ab95cede64](https://user-images.githubusercontent.com/84274432/155377430-5f74accb-ccf8-45c2-aede-90dc94d0a242.png)
![151690874-8cd02018-d350-4e8d-8297-2f5998956fda](https://user-images.githubusercontent.com/84274432/155377578-34ac575d-6735-4587-a013-11ed030895a8.png)

# Code 
```
#define IR A0
#define buzz 2
#define led1 3
#define led2 4
int x=0;
void setup() {
  pinMode(IR,INPUT);
  pinMode(buzz,OUTPUT);
  pinMode(led1,OUTPUT);
  pinMode(led2,OUTPUT);
  Serial.begin(9600);
  }

void loop() {
  x=analogRead(IR);
  delay(1000);
  Serial.println(x);
  if (x>=200){
    digitalWrite(buzz,HIGH);
    digitalWrite(led1,HIGH);
    digitalWrite(led2,LOW);
  }
  else{
    digitalWrite(buzz,LOW);
    digitalWrite(led2,HIGH);
    digitalWrite(led1,LOW);
  }
}
```
# Output
![exp8_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155540894-191a1e52-e799-456f-9e65-14b22d524016.gif)

# Experiment 9 : LDR Light Sensor

> An experiment to understand the working of an LM35 temperature Sensor.

## LM35 : Temperature Sensor

> LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.
> LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

# LM35
![151696955-95fe5f7c-0135-4473-a749-176059182951](https://user-images.githubusercontent.com/84274432/155541414-514ae2e6-8377-4834-a694-87ac88965cb2.png)

![151696973-b93b9154-405d-4f03-9f4b-5735642f37b1](https://user-images.githubusercontent.com/84274432/155541425-42cfe984-d218-426a-b514-2dc9f95e2e09.png)


# Components Required

- Arduino Uno Board
- LM35 x 1
- GREEN LED x 1
- RED LED x 1
- Breadboard x 1
- Conneting wires
- Buzzer x 1

# Circuit Diagrams

![151697013-df2d6407-13a9-489c-80ba-d55fb8c82992](https://user-images.githubusercontent.com/84274432/155541767-655897db-17fd-4e80-8de2-cbf028d1fe67.png)

# Code

```
#define sensor A0
int LEDR=4;
int LEDG=3;
int BUZZ=1;

void setup()
{
  pinMode(LEDR, OUTPUT);
  pinMode(LEDG, OUTPUT);
  pinMode(BUZZ,OUTPUT);

}
  void loop(){
    int reading = analogRead(sensor);
    float voltage = reading * (5.0 / 1024.0);
    float temp = (voltage - 0.5) * 100;
  
  if(temp<=50)
  {
     digitalWrite(LEDR,LOW);
    digitalWrite(LEDG,HIGH);
    digitalWrite(BUZZ,LOW);
  
  }
  else{
     digitalWrite(LEDG,LOW);
     digitalWrite(LEDR,HIGH);
      digitalWrite(BUZZ,HIGH);
 
   }
}

```
# Output

![151697054-4e2df17b-b741-49d9-823d-d90c32635ae3](https://user-images.githubusercontent.com/84274432/155542060-45a391ab-9838-41de-ba32-2e2c682a4c95.png)

# Video

![exp9_AdobeCreativeCloudExpress (1)](https://user-images.githubusercontent.com/84274432/155543855-53212f8a-d98c-4956-ac0c-07865138f4be.gif)

# Experiment 10 : IR Remote Control Using TSOP


> An experiment to understand the working of TSOP1738.

# TSOP1738 : IR Receiver Module

> The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.

# TSOP1738


![151707408-f39d11f9-cd72-40a0-bfc9-263f3508100e](https://user-images.githubusercontent.com/84274432/155544391-bc038c7f-10a4-430f-9b12-32fd1d123c6e.png)

# Components Required

- Arduino Uno Board
- TSOP1738 x 1
- GREEN LED x 2
- RED LED x 2
- YELLOW LED x 2
- Breadboard x 1
- Jumper wires x 10
- Remote x 1



# Circuit Diagrams

![151707484-4938121b-6107-4243-9161-ae8b4b786cf4](https://user-images.githubusercontent.com/84274432/155544760-ecc6d086-2d9e-44e1-a543-4f035d5f637c.png)


# Code
```
#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x00FF6897;
long off1 = 0x00FF9867;
long on2 = 0x00FFB04F;
long off2 = 0x00FF30CF;
long on3 = 0x00FF18E7;
long off3 = 0x00FF7A85;
long on4 = 0x00FF10EF;
long off4 = 0x00FF38C7;
long on5 = 0x00FF5AA5;
long off5 = 0x00FF42BD;
long on6 = 0x00FF4AB5;
long off6 = 0x00FF52AD;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if((i%2)==1){
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on =!on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13,on?HIGH:LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}                          

```
# Experiment 11 : Potentiometer analog Value Reading


> An experiment to understand the working of a potentiometer.

# POT-Potentiometer

> Potentiometer also known as POT is a variable resistor used in different circuit applications.

# POT

![151710934-5af0ac0c-0169-4833-b06a-15d489c8a649](https://user-images.githubusercontent.com/84274432/155545507-a7bfcd0b-2afe-44b0-9438-e7261dd5ceee.png)


# Components Required

- Arduino Uno Board
- Potentiometer x 1
- YELLOW LED x 1
- Breadboard x 1
- Jumper wires x 5


# Circuit Diagrams

![151710991-86c53818-2583-4768-bde3-505553047a05](https://user-images.githubusercontent.com/84274432/155545891-d24f24bd-b2df-4308-8c83-c79a06d39c24.png)

Code
```
#define pot A0
#define led 11
int x=0;
void setup() {
  pinMode(pot,INPUT);
  pinMode(led,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  x=analogRead(pot);
  analogWrite(led,x);
  Serial.println(x);
  delay(50);
}

```
# Output


![exp11_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/84274432/155546971-be2bd59b-bf7d-433d-bb11-ec26d4a34826.gif)


# Experiment 12 : 7 Segment Display

> An experiment to understand the working of 7 Segment Display.

# 7 Segment Display
> LED segment display is a semiconductor light-emitting device. Its basic unit is a light-emitting diode (LED). LED segment display can be divided into 7-segment display and 8-segment display according to the number of segments. 8-segment display has one more LED unit ( for decimal point display) than 7-segment one. Here I used Tinkercad platform for stimulating the circuit



![151802511-2d9733d7-1e01-440c-942b-6afa70a27d05](https://user-images.githubusercontent.com/84274432/155547264-281891b6-75a8-49ee-a4f9-25a98f11455f.png)


![151802682-0742507f-4ec6-4fe1-8db9-c1f58d0b731b (1)](https://user-images.githubusercontent.com/84274432/155547410-0cb784e5-8b65-4f4f-acd1-973ad8b96b7c.png)

# Components Required

- Arduino Uno Board
- 7 Segment display x 1
- 220ohm resistors x 7
- connecting wires

# Circuit Diagrams
![151803806-1eff36ac-53e7-44b6-b99b-c84b92330d61](https://user-images.githubusercontent.com/84274432/155547739-3de4104f-53bb-4f89-8901-f6e591018662.png)



# Code
```
int a = 13;     
int b = 12;      
int c = 11;    
int d = 10;    
int e = 9;     
int f = 8;    
int g = 7;

void setup() {                
 
pinMode(a, OUTPUT);      pinMode(b, OUTPUT);     pinMode(c, OUTPUT);
pinMode(d, OUTPUT);      pinMode(e, OUTPUT);     pinMode(f, OUTPUT);
pinMode(g, OUTPUT);
}


void loop() {

  digitalWrite(a, HIGH);
  digitalWrite(b, HIGH);
  digitalWrite(c, HIGH);
  digitalWrite(d, HIGH);       //Generating 1
  digitalWrite(e, LOW);
  digitalWrite(f, LOW);
  digitalWrite(g, HIGH);
  delay(1000);              
  digitalWrite(a, LOW);
  digitalWrite(b, LOW);
  digitalWrite(c, HIGH);      //Generating 2
  digitalWrite(d, LOW);
  digitalWrite(e, LOW);
  digitalWrite(f, HIGH);
  digitalWrite(g, LOW);
  delay(1000);              
  digitalWrite(a, LOW);
  digitalWrite(b, LOW);
  digitalWrite(c, LOW);
  digitalWrite(d, LOW);      //Generating 3
  digitalWrite(e, HIGH);
  digitalWrite(f, HIGH);
  digitalWrite(g, LOW);
  delay(1000);               
  digitalWrite(a, HIGH);
  digitalWrite(b, LOW);
  digitalWrite(c, LOW);
  digitalWrite(d, HIGH);
  digitalWrite(e, HIGH);     //Generating 4
  digitalWrite(f, LOW);
  digitalWrite(g, LOW);
  delay(1000);            
  digitalWrite(a, LOW);
  digitalWrite(b, HIGH);
  digitalWrite(c, LOW);
  digitalWrite(d, LOW);
  digitalWrite(e, HIGH);     //Generating 5
  digitalWrite(f, LOW);
  digitalWrite(g, LOW);
  delay(1000);            
  digitalWrite(a, LOW);
  digitalWrite(b, HIGH);
  digitalWrite(c, LOW);
  digitalWrite(d, LOW);    //Generating 6
  digitalWrite(e, LOW);
  digitalWrite(f, LOW);
  digitalWrite(g, LOW);
  delay(1000);               // wait for a second
  digitalWrite(a, LOW);
  digitalWrite(b, LOW);
  digitalWrite(c, LOW);
  digitalWrite(d, HIGH);
  digitalWrite(e, HIGH);   //Generating 7
  digitalWrite(f, HIGH);
  digitalWrite(g, HIGH);
  delay(1000);             
  digitalWrite(a, LOW );
  digitalWrite(b, LOW);
  digitalWrite(c, LOW);
  digitalWrite(d, LOW);
  digitalWrite(e, LOW);     //Generating 8
  digitalWrite(f, LOW);
  digitalWrite(g, LOW);
  delay(1000);            
  digitalWrite(a, LOW);
  digitalWrite(b, LOW);
  digitalWrite(c, LOW);
  digitalWrite(d, HIGH);
  digitalWrite(e, HIGH);    //Generating 9
  digitalWrite(f, LOW);
  digitalWrite(g, LOW);
  delay(1000);             
}

```

# Output 
![151804184-8957bf07-d72e-4565-a6ae-3015635c937e](https://user-images.githubusercontent.com/84274432/155548780-e41e8b8a-d26f-4574-985e-d83d91c62069.png)

# Assignment 1 : Night LED

> Automatic night lamp model using LDR and LED.

# Components Required

- Arduino Uno Board
- LDR x 1
- RED LED x 1
- Breadboard x 1
- Connection Wires


# Circuit Diagrams

![151858988-5fd53128-0227-4edf-aa8a-7ac2bf674d1b](https://user-images.githubusercontent.com/84274432/155549875-79a3faaa-9b4f-47a9-b94c-2fc2c5275599.png)

# Code

```
#define ldr A0
#define led 2
int x;
void setup() {
  pinMode(ldr, INPUT);
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}
void loop() {
  x=analogRead(ldr);
  Serial.println(x);
  if(x>=100){
    digitalWrite(led,HIGH);
    Serial.println("HIGH");
  }
  else{
    digitalWrite(led,LOW);
    Serial.println("LOW");
  }
  }
```

# Assignment 2 : Digital dice
 
> A digital dice using 6 LEDs and 1 push button.

# Components Required

- Arduino Uno Board
- Push button x 1
- RED LED x 6
- Breadboard x 1
- Connection Wires

# Circuit Diagrams
![151860133-f2ef6985-0542-4e24-8c5f-db4a2aac73ed](https://user-images.githubusercontent.com/84274432/155550668-c2139a36-1b79-4cd9-b3b0-81ecf1049187.png)



# Code 


```


#define DEBUG 0
int first = 2;
int second = 3;
int third = 4;
int fourth = 5;
int fifth = 6;
int sixth = 7;
int button = 8;
int pressed = 0;

void setup() {
  for (int i=first; i<=sixth; i++) {
    pinMode(i, OUTPUT);
  }
 
  pinMode(button, INPUT);
  
  randomSeed(analogRead(0));
  #ifdef DEBUG
    Serial.begin(9600);
  #endif

}

void buildUpTension() {
  for (int i=first; i<=sixth; i++) {
    if (i!=first) {
      digitalWrite(i-1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
  // right to left
  for (int i=sixth; i>=first; i--) {
    if (i!=sixth) {
      digitalWrite(i+1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
}

void showNumber(int number) {
  digitalWrite(first, HIGH);
  if (number >= 2) {
    digitalWrite(second, HIGH);
  }
  if (number >= 3) {
    digitalWrite(third, HIGH);    
  }
  if (number >= 4) {
    digitalWrite(fourth, HIGH);    
  }
  if (number >= 5) {
    digitalWrite(fifth, HIGH);    
  }
  if (number == 6) {
    digitalWrite(sixth, HIGH);    
  }
}

int throwDice() {
  int randNumber = random(1,7);
  
  #ifdef DEBUG
    Serial.println(randNumber);
  #endif
  
  return randNumber;
}

void setAllLEDs(int value) {
  for (int i=first; i<=sixth; i++) {
    digitalWrite(i, value);
  }
}

void loop() {
  pressed = digitalRead(button);

  if (pressed == HIGH) {
    setAllLEDs(LOW);
    
    buildUpTension();
    int thrownNumber = throwDice();
    showNumber(thrownNumber);
  } 

}
```



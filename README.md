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
GREEN LED x 1
RED LED x 1
10k Resistor x 1



![151690868-ae0d09fd-c798-42e0-a970-07ab95cede64](https://user-images.githubusercontent.com/84274432/155377430-5f74accb-ccf8-45c2-aede-90dc94d0a242.png)
![151690874-8cd02018-d350-4e8d-8297-2f5998956fda](https://user-images.githubusercontent.com/84274432/155377578-34ac575d-6735-4587-a013-11ed030895a8.png)

# Code 
```



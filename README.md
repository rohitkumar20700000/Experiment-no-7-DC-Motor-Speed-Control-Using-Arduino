
###  DATE:05-04-2024 

###  NAME: M ROHIT KUMAR
###  ROLL NO :212221220045
###  DEPARTMENT:INFORMATION TECHNOLOGY
# Experiment-no-6-DC-Motor-Speed-Control-Using-Arduino
### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)

### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.

![image](https://user-images.githubusercontent.com/36288975/167763051-b230c183-afc5-46f2-ba95-0f95e10dd6c9.png)
FIGURE-01 H BRIDGE CIRUCIT INTERFACE 
 
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:
![image](https://user-images.githubusercontent.com/36288975/167763120-1421c2c5-8381-49eb-b376-03f6e1113b7a.png)
TABLE-01 EXITATION TABLE FOR H BRIDGE 

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
```
int in1=5;
int in2=6;
int en=3;
void setup()
{
  pinMode(in1,OUTPUT);
  pinMode(in2,OUTPUT);
  pinMode(en,OUTPUT);
}
void loop()
{
  analogWrite(en,220);
  
  digitalWrite(in1,LOW);
  digitalWrite(in2,HIGH);
  delay(500);
}
```

### OUTPUT
### FIG 1 CIRCUIT DIAGRAM

![Screenshot 2024-04-05 155715](https://github.com/rohitkumar20700000/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/130482461/16359554-5328-4a97-8102-6d56149829b5)

### FIG 2 SCHEMATIC DIAGRAM

![EX-06 Rohit kumar M (212221220045)_page-0001](https://github.com/rohitkumar20700000/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/130482461/a888d9f2-30c5-44bd-b475-d435eaa4445e)



### GRAPH AND TABULATION 

### FIG 3 TABULATION

![exp 6 table](https://github.com/dineshdk154/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/104413084/ca6c05f2-252b-4d10-ba2f-d06a4396a782)

### FIG 4 GRAPH

![exp 6 graph](https://github.com/dineshdk154/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/104413084/df6f1952-20c2-480c-805d-1c5fc20cc2d1)

### RESULT

Control the speed and the direction of a DC motor using L293D driver ic( H- bridge) is learned

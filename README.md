###  DATE: 5/04/2024

###  NAME: Divya R
###  ROLL NO :212222040040
###  DEPARTMENT:CSE
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
int input1=5;
int input2=6;
int en=3;

void setup()
{
  pinMode(input1, OUTPUT);
  pinMode(input2, OUTPUT);
  pinMode(en, OUTPUT);
}


void loop()
{ 
  analogWrite(en,50);
 
  digitalWrite(input1, LOW);
  digitalWrite(input2, HIGH);
  delay(500);
}
```

### OUTPUT

CIRCUIT DIAGRAM

![Screenshot 2024-04-06 174726](https://github.com/divyadivya10/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560271/a11e951f-ba9e-4b80-8afc-2fa76583a38a)


SCHEMATIC DIAGRAM

![Screenshot 2024-04-06 174812](https://github.com/divyadivya10/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560271/06a57795-b92b-47a2-8e54-745c6d4582f4)

TABULATION

 ![WhatsApp Image 2024-04-05 at 16 21 35_d07c9a12](https://github.com/divyadivya10/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560271/e78f19a9-40e0-4bcf-8e2c-0a03c650061d)

 GRAPH

 ![WhatsApp Image 2024-04-05 at 16 21 30_9cae2841](https://github.com/divyadivya10/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560271/6a1e3478-a761-4aea-85de-945b44bf84ee)





### RESULTS AND DISCUSSION 
Thus, the speed and the direction of a DC motor using L293D driver ic( H- bridge) is controlled.




# EXPERIMENT NO 05 INTERFACING ANALOG OUTPUT SERVO MOTOR WITH ARDUINO

### AIM
To interface an Analog output (servo motor) and modify the angular displacement of the servo using PWM signal .
COMPONENTS REQUIRED:
1.	Servo motor of choice (9v is preferred )
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	Servo rated power supply (dc source )


### THEORY
Servo motors and are constructed out of basic DC motors, by adding:
•	 gear reduction
•	 a position sensor for the motor shaft
•	 an electronic circuit that controls the motor's operation
Typically, a potentiometer (variable resistor) measures the position of the output shaft at all times so the controller can accurately place and maintain its setting.
Servo motors are used for angular positioning, such as in radio control airplanes.  They typically have a movement range of 180 deg but can go up to 210 deg.The output shaft of a servo does not rotate freely, but rather is made to seek a particular angular position under electronic control. 


![image](https://user-images.githubusercontent.com/36288975/163544439-1f477927-fcd4-42f0-9ce4-c863fdbf1210.png)



#### Figure-01 SERVO MOTOR SPLIT VIEW 
Control 
An external controller (such as the Arduino) tells the servo where to go with a signal know as pulse proportional modulation (PPM) or pulse code modulation (which is often confused with pulse width modulation, PWM). PWM uses 1 to 2ms out of a 20ms time period to encode its information.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/163544482-3027136f-7135-4f3d-a23f-8dc2fe04194d.png)

### Figure-02 SERVO MOTOR PINS

 ![image](https://user-images.githubusercontent.com/36288975/163544513-ca497421-e6ba-4f91-871f-5cfba77f22a8.png)


### Figure-03 SERVO MOTOR OVERVIEW 

 


 





CIRCUIT DIAGRAM
 
 
 ![image](https://user-images.githubusercontent.com/36288975/163544618-6eb8a7b5-7f1a-428a-8d9f-fd899b145efb.png)

### FIGURE 04 CIRCUIT DIAGRAM

### PROCEDURE:
1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device.


### PROGRAM :
~~~
Name: S Adithya Chowdary.

reg no:212221230100.

#include<Servo.h>
Servo s1;
void setup()
{
  s1.attach(9);
}
void loop()
{
  for (int i=0;i<=180; i+= 1)
  {
    s1.write(i);
    delay(15);
  }
  for (int i=180;i>=0;i-= 1)
  {
    s1.write(i);
    delay(15);
  }
}

~~~
### Circuit Diagram:
### Offset:
![r1](https://user-images.githubusercontent.com/94296221/194714314-6aa1b546-b92f-4db7-9f25-f310443bd54d.png)

### Onset:
![r2](https://user-images.githubusercontent.com/94296221/194714317-3c180a4c-3c81-4d44-a715-30a6ddcbc907.png)

### Output:
### Serial monitor:
![r3](https://user-images.githubusercontent.com/94296221/194714482-b8fa22e4-b1db-4612-abd2-419758214d4b.png)
### Toggle graph:
![r4](https://user-images.githubusercontent.com/94296221/194714522-243c471f-c21e-47fe-a6bd-a5243899c9a2.png)

### RESULTS: 
Arduino uno interfacing with servo motor is learned and angular position is controlled using PWM signal.

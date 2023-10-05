# Automatic Street Light Controller

##  AIM:
To design and implement Automatic Street Light controller using Arduino UNO controller.

## Software required:
Arduino IDE </br>
Proteous

## PROCEDURE:
### Arduino IDE
Step1:Open the Arduino IDE </br>
Step2: Go to file and select new file option </br>
Step3:Type the program </br>
Step4:Go to file and select save option to save the program </br>
Step5:Go to sketch and select verify or compile options </br>
Step6:If no error Hex file will be generated in the temporary folder </br>
### Proteus
Step7:Open the Proteus software </br>
Step8:Go to file select new design and click ok button </br>
Step9:Select component mode and click pick devices from the library </br>
Step10:Type the component name in the keyword to select the components and click ok button </br>
Step11:Design the circuit as per the diagram </br>
Step12:Double click the Arduino controller and upload the hex file generated by Arduino IDE </br>
Step13:Click start button and check the output

## THEORY:

The Street lights are the major requirements in today’s life for safety purposes and avoiding accidents during night. Providing street lighting is one of the most important and expensive responsibilities of a city. Lighting can account for 10-38% of the total energy bill in typical cities worldwide. Street lighting is a particularly critical concern for public authorities in developing countries because of its strategic importance for economic and social stability. The fixtures of street lights indirectly have assisted the public and government in reduction of crime rate and accidents in the area. It also encourages social inclusion by providing an environment in which people feel they can walk in hours of darkness. Despite that in today’s busy lifestyle no one bothers to switch it OFF/ON when not required. Inefficient lighting wastes significant financial resources each year, and poor lighting creates unsafe conditions. Energy efficient technologies and design can cut street lighting costs dramatically. The main consideration in the present field technologies are Automation, Power consumption and cost effectiveness. Automation is intended to reduce man power with the help of intelligent systems. Power saving is the main consideration forever as the sources of the power are getting diminished due to various reasons. Designing a costefficient system is very important as the requirement is more. In order to overcome this problem, automatic street light control methods is introduced. The main objective of our project is to provide a better solution to minimize the electrical wastage in operating street lights, in this era of automation humans are restless and are not in a position to regulate the manual operations in any field, a rapid advancement in embedded systems has paved path for the design and development of microcontroller based automatic control systems. Our project presents an automatic street light controller using light dependent resistor(LDR). By using this system manual works are removed. The street lights are automatically switched ON when the sunlight goes below the visible region of our eyes. It automatically switches OFF the street lights under illumination by sunlight. It is a simple and powerful concept, to switch ON/OFF the street light system automatically. It automatically switches ON the streetlight when the sunlight goes below the visible region of our eyes and switches OFF the streetlight when ample amount of sunlight is available. The component used for light sensing is a Light Dependent Resistor. By using the LDR we can operate the streetlight automatically, when ample amount of light is available the streetlight will be in the OFF state and when it is dark the light will be in ON state, it means .LDR resistance is inversely proportional to light falling on it. When the light falls on the LDR it sends the commands to the control circuit that it should be in the OFF state and the streetlight turns OFF. This project exploits the working of a transistor in saturation region and cut-off region to switch ON and switch OFF the lights at appropriate time with the help of an electromagnetically operated switch. This system operates in accordance with the varying sunlight, whenever there is sufficient light falling on the LDR, it exhibits high resistance and acts as an insulator and in darkness the LDR behaves as low resistance path and allows the flow of electricity. The switching operation of streetlight is carried out by ATmega8 microcontroller along with relay driver circuit. The entire control circuit requires a regulated 5V DC for its operation. A step down transformer is used to step down the 230V AC from mains into 12V AC, this 12V AC is converted into 5V DC by using a bridge rectifier, and the controlled output from the voltage regulator is sent to the control circuit. Light Dependent Resistor LDRs or Light Dependent Resistors are very useful especially in light/dark sensor circuits. Normally the resistance of an LDR is very high, sometimes as high as 1000000 ohms, but when they are illuminated with light resistance drops dramatically. Photo sensors are the devices that alter their electrical characteristics, in the presences of visible or invisible light. The best-known devices of this type are the light dependent resistor, the photo diode and the phototransistors. Light dependent resistor as the name suggests depends on light for the variation of resistance. LDR are made by depositing a film of cadmium sulphide or cadmium selenide on a substrate of ceramic containing no or very few free electrons when not illuminated. The longer the strip the more the value of resistance. When light falls on the strip, the resistance decreases. In the absence of light the resistance can be in the order of 10kΩ to 15kΩ and is called the dark resistance. Depending on the exposure of light the resistance can fall down to value of 500 Ω. Light dependent resistors are available as discs 0.5cm to 2.5cm. The resistance rises to several Mega ohms under dark conditions. 

![image](https://github.com/anishkumar-Embedded/Implementation-of-Automatic-Street-Light-Controller/assets/71547910/f0f6faa2-b54a-440d-8a76-d8c6deb49827)

The figure-1 shows that when the torch is turned on, the resistance of the LDR decreases, and allows the current to pass through it. The LDR are made of High resistance semiconductor, when light fall on such a semiconductor; the bound electrons gets the light energy from incident photons. Due to this additional energy these electron become free and jump into conduction band. The electron hole pairs are generated. Due to these charge carries the conductivity of LDR increases, increasing its resistivity. The device consists of a pair of metal film contacts separated by a snakelike track of cadmium sulphide film, designed to provide the maximum possible contact area with the two metal films. The structure is housed in a clear plastic or resin case, to provide free access to external light. LDRs are the light dependent resistors available in the market which are used for practical implications in various electronic circuits. Practical LDRs are available in variety of sizes and package styles, the most popular size is having a face diameter of roughly 10mm. 

![image](https://github.com/anishkumar-Embedded/Implementation-of-Automatic-Street-Light-Controller/assets/71547910/9099c14f-7ec4-4332-93b8-6354dd03c2d7)

LDR Features of LDR are as follows: 
1. High reliability. 2. Light weight. 3. Wide spectral response. 4. Wide ambient temperature range.


## PROGRAM:
```
    int sensorPin = A0; 
    int sensorValue = 0; 
   void setup() 
   {
  Serial.begin(9600); 
  pinMode(13, OUTPUT);
 }
 void loop() 
 {
  sensorValue = analogRead(sensorPin);
  Serial.print("OUTPUT:");
  Serial.println(sensorValue); 
   delay(500);
  if(sensorValue>=550)
  {
  digitalWrite(13, HIGH);  
   delay(5000);
    }
  else
  {
   digitalWrite(13, LOW);  
   delay(5000);
    }
  }
```
## CIRCUIT DIAGRAM:


![image](https://github.com/gokul-sureshkumar/Implementation-of-Automatic-Street-Light-Controller/assets/121148715/85e3aac1-34be-44b7-84c7-d6bfd4d1102a)

## OUTPUT:

![image](https://github.com/gokul-sureshkumar/Implementation-of-Automatic-Street-Light-Controller/assets/121148715/971bd531-659d-4ddb-9cbe-0a1fdccfb660)

## RESULT:
Thus the Automatic Street Light controller was implemented using Arduino UNO controller.

---
name: Grove - Turbidity Sensor (Meter) for Arduino V1.0
category: sensor
bzurl: 
surveyurl: 
sku: 101020752
tags:
---


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Turbidity-Sensor/master/img/Grove-Turbidity-Sensor-wiki.jpg)


The Grove turbidity sensor can measure the turbidity of the water (the number of suspended particles).

 
The optical sensor of this module can measure the density of turbid water and the concentration of extraneous matter using the refraction of wavelength between photo transistor and diode. By using an optical transistor and optical diodes, an optical sensor measures the amount of light coming from the source of the light to the light receiver, in order to calculate turbidity of water.

 
The output mode can be selected by adjusting the switch on the board. Supports analog and digital output. The sensitivity can be adjusted by the on-board knob.


<p style=":center"><a href="https://www.seeedstudio.com/Grove-Turbidity-Sensor-p-4399.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>


## Features

 - Low power consumption
 - Small size: 2.0cm x 4.0cm Grove module
 - Only 3 pins needed, save I/O resources
 - Easy to use: Grove connector, plug and play
 - Output mode optional, support analog output and digital output


!!!Tip

    More details about Grove modules please refer to [Grove System](http://wiki.seeedstudio.com/Grove_System/)




## Specification

|Parameter|Value/Range|
|---|---|
| Operating Voltage |	3.3V/5V DC |
| Output Interface  | Analog<br>Digital |
| Connector | 1 Grove<br>1 Power interface |
| Size   | 20*40mm |


## Typical applications

- Measure the water pollution degree of washing machines such as dishwashers to determine the optimal washing time and rinsing times.
- Industrial site control.
- Environmental wastewater treatment.


## Hardware Overview


![](https://github.com/SeeedDocument/Grove-Turbidity-Sensor/raw/master/img/Grove-Turbidity-Sensor-pin.jpg)

- **Digital to Analog Switch**

  - "D" is the digital output, the threshold of high and low level can be adjusted by on-board knob.
  - "A" is the analog output, the output value will decrease with the increase of liquid turbidity.




## Platforms Supported


| Arduino| Raspberry Pi| BeagleBone| Wio| LinkIt ONE|
|--------|-------------|-----------|----|-----------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |


!!!Caution  

    The platforms mentioned above as supported is/are an indication of the module's software or theoritical compatibility. We only provide software library or code examples for Arduino platform in most cases. It is not possible to provide software library / demo code for all possible MCU platforms. Hence, users have to write their own software library.




## Getting Started


### Play With Arduino


!!!Note

    If this is the first time you work with Arduino, we firmly recommend you to see [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.




**Materials required**


| Seeeduino V4.2 | Grove - Turbidity Sensor | Base Shield |
|--------------|----------------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Turbidity-Sensor/master/img/Grove-Turbidity-Sensor.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|
|[Get One Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get One Now](https://www.seeedstudio.com/Grove-Turbidity-Sensor-p-4399.html)|[Get One Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|


!!!Note


	**1** Please plug the USB cable gently, otherwise you may damage the port. Please use the USB cable with 4 wires inside, the 2 wires cable can't transfer data. If you are not sure about the wire you have, you can click [here](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html) to buy. 
    
	**2** Each Grove module comes with a Grove cable when you buy. In case you lose the Grove cable, you can click [here](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html) to buy.


#### Analog Output


##### Hardware Connection


- **Step 1.** The switch on the sensor selects **A**.

- **Step 1.** Connect Grove - Turbidity Sensor to port **A0** of Grove-Base Shield.

- **Step 2.** Plug Grove - Base Shield into Seeeduino.

- **Step 3.** Connect Seeeduino to PC via a USB cable.


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Turbidity-Sensor/master/img/connect.jpg)


!!!Note   
     
    If we don't have Grove Base Shield, We also can directly connect Grove - Turbidity Sensor to Seeeduino as below.





| Seeeduino     | Grove - Turbidity Sensor|
|---------------|-------------------------|
| 5V            | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| A0            | Yellow                  |



##### Software


- **Step 1.** Copy the code below into Arduino IDE and upload. If you do not know how to upload the code, please check [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```c
void setup() {

  Serial.begin(9600); //Baud rate: 9600
}

void loop() {
  int sensorValue = analogRead(A0);// read the input on analog pin 0:
  float voltage = sensorValue * (5.0 / 1024.0); // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
  Serial.println(voltage); // print out the value you read:
  delay(500);
}

```


- **Step 2.** Open the **Serial Monitor** of Arduino IDE by click **Tool-> Serial Monitor** or tap the **Ctrl+Shift+M** key at the same time. Set the baud rate to **9600**.


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Turbidity-Sensor/master/img/result.png)


- **Step 3.**  Now you can use this sensor, and the output will be like this:


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Turbidity-Sensor/master/img/serial-port.png)


#### Digital Output


##### Hardware Connection


- **Step 1.** The switch on the sensor selects **D**.

- **Step 1.** Connect Grove - Turbidity Sensor to port **D2** of Grove-Base Shield.

- **Step 2.** Plug Grove - Base Shield into Seeeduino.

- **Step 3.** Connect Seeeduino to PC via a USB cable.




!!!Note   
     
    If we don't have Grove Base Shield, We also can directly connect Grove - Turbidity Sensor to Seeeduino as below.





| Seeeduino     | Grove - Turbidity Sensor|
|---------------|-------------------------|
| 5V            | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| D2            | Yellow                  |



##### Software


- **Step 1.** Copy the code below into Arduino IDE and upload. If you do not know how to upload the code, please check [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```c
int ledPin = 3;               
int sensor_in = 2;                 // Turbidity sensor on Digital Pin 2

void setup(){
  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);      // Set ledPin as output mode
  pinMode(sensor_in, INPUT);       //Set Turbidity sensor pin to input mode
}

void loop(){
   int sensorValue = digitalRead(sensor_in);
   Serial.println(sensorValue);
   if(sensorValue==HIGH){       //Read sensor signal 
        digitalWrite(ledPin, HIGH);   // if sensor is LOW, then turn on
     }else{
        digitalWrite(ledPin, LOW);    // if sensor is HIGH, then turn off the led
     }
    delay(500);
}
```


- **Step 2.** We use digital output and raise or lower the trigger by adjusting the potentiometer to make the LED turn on and off.


## Schematic Online Viewer


<div class="altium-ecad-viewer" data-project-src="https://github.com/SeeedDocument/Grove-Turbidity-Sensor/raw/master/res/Grove-Turbidity-Sensor-v1.0.zip" style="border-radius: 0px 0px 4px 4px; height:500px; border-style: solid; border-width: 1px; border-color: rgb(241,241, 241); overflow: hidden; max-width: 1280px; max-height: 700px; box-sizing: border-box;" /></div>


## Resources


- **[ZIP]** [Schematic Diagram](https://github.com/SeeedDocument/Grove-Turbidity-Sensor/raw/master/res/Grove-Turbidity-Sensor-v1.0.zip)

- **[PDF]** [LMV358 Datasheet](https://github.com/SeeedDocument/Grove-Turbidity-Sensor/raw/master/res/LMV358-Datasheet.pdf)

- **[PDF]** [MPX5700AP Datasheet](https://github.com/SeeedDocument/Grove-Turbidity-Sensor/raw/master/res/Turbidity-Sensor-Datasheet.pdf)





## Tech Support


Please submit any technical issue into our [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>

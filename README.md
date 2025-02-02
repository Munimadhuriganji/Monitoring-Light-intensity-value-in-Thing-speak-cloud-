## NAME : GANJI MUNI MADHURI
## REG NO : 212223230060
# EX - 04 Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-.

# AIM:
To monitor and upload the light intensity value in the Things mate using Arduino controller.

# Apparatus required:
Arduino Controller  </br>
Indoor gateway</br>
LoRaWAN shield </br>
LDR </br>
Power supply </br>
Connecting wires </br>
Bread board </br>

# PROCEDURE:

### Procedure for gateway setup
	Go to the link http://172.31.255.254:8000 </br>
	Type the user name password </br>
	Go to LoRa and set the frequency plan 865 Mhz </br>
	In LoRa WAN configurations enter the Gate EUI and server address </br>
	Enable the Internet </br>
	Select the Wifi access point </br>
	Type the ssid and password in wifi LAN setting </br>
	Select the internet and IoT service and provide the details. </br>
	Check all the green colour tick marks in gate way and proceed </br>
### Procedure for gateway registration in The thingsMate LoRaWAN Management </br>
	Login https://iot.saveetha.in:4433 and provide the user id and password </br>
	Go to overview and select application server </br>
	Go to gateway and add new gateway </br>
	Enter the gateway id, name, EUI and select frequency plan </br>
	Open Arduino IDE and type the program for the given application </br>
	Compile the program if no error uploads the program in the controller </br>
	Go to gateways in things mate and check the live data </br>
	Create channel by giving channel name and ID </br>
	Add end device and enter the frequency plan, DevEUI, AppEUI, APP key, Select LoRaWAN version </br>
	Enter payload formatters </br>
	Go to the option query and give the new query name </br>
	Go to the option Dashboard and verify the output.</br>  

# THEORY:

### What is IoT?

Internet of Things (IoT) describes an emerging trend where a large number of embedded devices (things) are connected to the Internet. These connected devices communicate with people and other things and often provide sensor data to cloud storage and cloud computing resources where the data is processed and analyzed to gain important insights. Cheap cloud computing power and increased device connectivity is enabling this trend.IoT solutions are built for many vertical applications such as environmental monitoring and control, health monitoring, vehicle fleet monitoring, industrial monitoring and control, and home automation

![image](https://user-images.githubusercontent.com/71547910/235334044-c01d4261-d46f-4f62-b07f-72a7b6fce5d5.png)

### LDR

LDR (Light Dependent Resistor) as the name states is a special type of resistor that works on the photoconductivity principle means that resistance changes according to the intensity of light. Its resistance decreases with an increase in the intensity of light.It is often used as a light sensor, light meter, Automatic street light, and in areas where we need to have light sensitivity. LDR is also known as a Light Sensor. LDR are usually available in 5mm, 8mm, 12mm, and 25mm dimensions.

The Light-dependent resistors made with photosensitive semiconductor materials like Cadmium Sulphides (CdS), lead sulfide, lead selenide, indium antimonide, or cadmium selenide and they are placed in a Zig-Zag shape.Two metal contacts are placed on both ends of the Zig-Zag shape these metal contacts help in creating a connection with the LDRs.Now, a transparent coating is applied on the top so that the zig-zag-shaped photosensitive material gets protected and as the coating is transparent the LDR will be able to capture light from the outer environment for its working.

![image](https://github.com/anishkumar-Embedded/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/71547910/26a0e210-5d9d-40c6-955d-89c637d38265)

#### LDR Working Principle

It works on the principle of photoconductivity whenever the light falls on its photoconductive material, it absorbs its energy and the electrons of that photoconductive material in the valence band get excited and go to the conduction band and thus increasing the conductivity as per the increase in light intensity.Also, the energy in incident light should be greater than the bandgap gap energy so that the electrons from the valence band got excited and go to the conduction band.The LDR has the highest resistance in dark around 1012 Ohm and this resistance decreases with the increase in Light.As per the property of LDRs, the amount of light entering the LDR the inversely proportional to the resistance of the sensor, and the graph is hyperbolic in nature.

![image](https://github.com/anishkumar-Embedded/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/71547910/e7c513a2-8aca-4f6a-bf20-32e1eeff3e17)


### What is LoRaWAN

The LoRaWAN® specification is a Low Power, Wide Area (LPWA) networking protocol designed to wirelessly connect battery operated ‘things’ to the internet in regional, national or global networks, and targets key Internet of Things (IoT) requirements such as bi-directional communication, end-to-end security, mobility and localization services.LoRaWAN® network architecture is deployed in a star-of-stars topology in which gateways relay messages between end-devices and a central network server. The gateways are connected to the network server via standard IP connections and act as a transparent bridge, simply converting RF packets to IP packets and vice versa. The wireless communication takes advantage of the Long Range characteristics of the LoRaÒ physical layer, allowing a single-hop link between the end-device and one or many gateways. All modes are capable of bi-directional communication, and there is support for multicast addressing groups to make efficient use of spectrum during tasks such as Firmware Over-The-Air (FOTA) upgrades or other mass distribution messages.

The specification defines the device-to-infrastructure (LoRa®) physical layer parameters & (LoRaWAN®) protocol and so provides seamless interoperability between manufacturers, as demonstrated via the device certification program.While the specification defines the technical implementation, it does not define any commercial model or type of deployment (public, shared, private, enterprise) and so offers the industry the freedom to innovate and differentiate how it is used.The LoRaWAN® specification is developed and maintained by the LoRa Alliance®: an open association of collaborating members.

![image](https://github.com/anishkumar-Embedded/Update-the-Ultrasonic-sensor-value-in-cloud/assets/71547910/c63c4edd-3b95-4a69-b9c2-4862afb335c3)

### Characteristics of LoRaWAN technology
Long range communication up to 10 miles in line of sight.
Long battery duration of up to 10 years. For enhanced battery life, you can operate your devices in class A or class B mode, which requires increased downlink latency.
Low cost for devices and maintenance.
License-free radio spectrum but region-specific regulations apply.
Low power but has a limited payload size of 51 bytes to 241 bytes depending on the data rate. The data rate can be 0,3 Kbit/s – 27 Kbit/s data rate with a 222 maximal payload size.

### The Things Mate - IoT Cloud Platform

IoT cloud platforms play a pivotal role in the development and deployment of Internet of Things (IoT) applications, connecting devices and enabling seamless data management and analysis. These platforms typically offer a comprehensive suite of services, including device provisioning, secure connectivity, data storage, and advanced analytics.Leading IoT cloud platforms, such as AWS IoT, Azure IoT, and Google Cloud IoT, provide scalable and reliable infrastructure to accommodate diverse IoT deployments. They facilitate device management, allowing users to monitor, update, and control connected devices remotely. Security features are integral, ensuring data integrity and safeguarding against potential threats.

Analytics capabilities enable organizations to derive meaningful insights from the vast amounts of data generated by IoT devices. Machine learning and artificial intelligence integrations further enhance predictive analytics, enabling proactive decision-making.These platforms often offer APIs for seamless integration with other cloud services, supporting a wide range of industries and applications, from smart homes to industrial automation. As the IoT landscape evolves, cloud platforms continue to innovate, contributing to the growth and sophistication of IoT ecosystems worldwide. Choosing the right IoT cloud platform involves considering factors such as scalability, security, and compatibility with specific use cases.

# PROGRAM:
```
#include <WiFi.h>

#include "ThingSpeak.h" // always include thingspeak header file after other header files and custom macros
#define ldr_pin 34
char ssid[] = "Sripriya";   // your network SSID (name) 
char pass[] = "123456789";   // your network password
int keyIndex = 0;            // your network key Index number (needed only for WEP)
WiFiClient  client;

unsigned long myChannelNumber =  2487109;
const int ChannelField = 1;
const char * myWriteAPIKey = "4TL0XDHT9DBX1YD4";

int ldrValue = 0;       // Variable to store raw analog value
int lightPercentage = 0;

const int darkValue = 4095; // Analog value in complete darkness
const int brightValue = 0;  


void setup() 
{
  Serial.begin(115200);  //Initialize serial
  pinMode(ldr_pin, INPUT);
  WiFi.mode(WIFI_STA);   
  ThingSpeak.begin(client);  // Initialize ThingSpeak
}

void loop() 
{
  // Connect or reconnect to WiFi
  if(WiFi.status() != WL_CONNECTED)
{
    Serial.print("Attempting to connect to SSID: ");
    
    while(WiFi.status() != WL_CONNECTED)
    {
      WiFi.begin(ssid, pass); 
      Serial.print(".");
      delay(5000);     
    } 
    Serial.println("\nConnected.");
  }

  /* LDR sensor */
  int ldrValue= analogRead(ldr_pin);  
  
  lightPercentage = map(ldrValue, darkValue, brightValue, 0, 100);

  // Constrain the percentage to 0-100 range
  lightPercentage = constrain(lightPercentage, 0, 100);
  Serial.println("Intensity="); //print on serial monitor using ""
  Serial.println(lightPercentage);    
  Serial.println("%");     //display output on serial monitor
  
  ThingSpeak.writeField(myChannelNumber, ChannelField, lightPercentage, myWriteAPIKey);
  delay(5000); 
}
```
# CIRCUIT DIAGRAM:
![image](https://github.com/user-attachments/assets/fbfe229b-a773-4b82-9f7c-5a37cc2eaa36)


# OUTPUT:
![WhatsApp Image 2024-11-16 at 14 49 26_153952aa](https://github.com/user-attachments/assets/3c736142-d155-4e07-a488-909125177e35)

# RESULT:

Thus the light intensity valve is uploaded in the Things mate using Arduino controller.

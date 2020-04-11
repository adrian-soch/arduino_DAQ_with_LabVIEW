# Creating a DAQ system with Arduino and LabVIEW
A tutorial on setting up an data acquisition system with an Arduino device and LabVIEW.


## Installation
- Download [LabVIEW](https://www.ni.com/en-ca/support/downloads/software-products/download.labview.html#329059) and [NI-VISA](https://www.ni.com/en-ca/support/downloads/drivers/download.ni-visa.html#329456). 

- Open the VI Package Manager, find and install **Digilent LINX**

![image](https://user-images.githubusercontent.com/6884645/79051249-32f3c400-7bfd-11ea-870c-5fb3e43f887e.png)


## Setup
- Connect your Arduino device and double check the port number (you can do this with the "Device Manager" in Windows)

![image](https://user-images.githubusercontent.com/6884645/79051347-b2819300-7bfd-11ea-9fb0-8c12cfc8f1d8.png)

- To setup the Arduino to send data to our labview program we need to configure the firmware. Go to tools/MakerHub/LINX/LINX Firmware Wizard

![image](https://user-images.githubusercontent.com/6884645/79050681-b1e6fd80-7bf9-11ea-9dee-9421554ffc41.png)

- Select your device and follow the steps. 

![image](https://user-images.githubusercontent.com/6884645/79050740-04281e80-7bfa-11ea-9c26-fcf3327ed741.png)

- Once the Wizard complete the process we can launch an example from the bottom right corner.

![image](https://user-images.githubusercontent.com/6884645/79050852-d0012d80-7bfa-11ea-9c22-8dad74e836ec.png)

**If you ran into issue getting to this step try [this](https://www.labviewmakerhub.com/doku.php?id=learn:tutorials:libraries:linx:getting_started) you can also try the LINX Firmware Wizard *Help* button or a simple internet search to help you out.**


## Test
- With the LINX Blink(Simple).vi open we are ready to test communication between the Arduino and LabVIEW
- Select the port connected to your device and press the *Run* arrow at the top right
- Clicking the green button should turn the built in LED on and off
-Click *Stop* to end the test

![image](https://user-images.githubusercontent.com/6884645/79052323-aac4ed00-7c03-11ea-88c0-d077f66befc4.png)


## Customize

After we have checked that the Arduino communicates with LabVIEW, it's time to create our own program. 

- Begin with an example, go to help/Find Examples

![image](https://user-images.githubusercontent.com/6884645/79051858-7ef43800-7c00-11ea-936f-bc5766da9543.png)

- Start with the example that is closest to your requirments and build it up from there
- The Front Panel has gauges and progress bars to visualize the data
- The Block Diagram sets 4 analog pins for reading data and recording to an excel file for analysis.

![image](https://user-images.githubusercontent.com/6884645/79051700-b0b8cf00-7bff-11ea-9095-5463ef462448.png)

![image](https://user-images.githubusercontent.com/6884645/79051649-44d66680-7bff-11ea-9aa5-4ea1cb856344.png)

# Universal Devices BASpi6U6R NodeServer

## Based on the Contemporary Controls BASpi SYS6U6R Controller

* Inputs UOM are set as for, AI-1-3 degrees Fahrenheit, AI-4 btu/h, AI-5 watts & AI-6 cfm.

![Single Exposure Poly](https://github.com/sjpbailey/UDI-BASpi-SYS6U6R-master/blob/master/Images%2FBASpi_img1.png)

* Test Program for outputs:

![ISY Output Test Program](https://github.com/sjpbailey/UDI-BASpi-SYS6U6R-master/blob/master/Images%2FBASpi6u6r_img2.png)

* It would be great if the Else statement also had a seperate If statement before it ran in the ISY line code. This is also a very diverse platform that is evolving.

## BASpi-SYS6U6R DIY BacNet Control Device by Contemporary Controls

* Main
[Contemporary Controls BASpi DIY](https://www.ccontrols.com/basautomation/baspi.php)
* BASpi 6U6R Controller
[Contemporary Controls BASpi 6U6R](https://www.ccontrols.com/pdf/ds/BASPI-datasheet.pdf)
* BASpi 6U6R Installation
[Contemporary Controls BASpi 6U6R Install](https://www.ccontrols.com/pdf/BASpi-hardware-install-guide.pdf)
* BASpi 6U4R2A Controller
[Contemporary Controls BASpi 6U4R2A](https://www.ccontrols.com/pdf/ds/BASPI-AO2-datasheet.pdf)
* BASpi 6U4R2A Installation
[Contemporary Controls BASpi 6U4R2A Install](https://www.ccontrols.com/pdf/TD180600.pdf)
* BASpi Controller Configuration
[Contemporary Controls BASpi Configuration Quick Start](https://www.ccontrols.com/pdf/is/BASPI-QSGuide.pdf)

### Why

* The purpose of this Nodeserver is for custom control for general Home automation for up to six 6, Binary Outputs and six 6 Universal Inputs. It utilizes the pip bascontrolns module for Contemporary Controls BAS line of DIY Devices. <https://pypi.org/project/bascontrolns/>

* It utilizing the Contemporary Controls BASpi SYS6U6R control Module.
Please see links above for information & configuration of this Device.

* This will be included in a Network series for custom home control for Irrigation, Pool, six 6 car garage door controller, HVAC, VVT, Boiler, Well along with any custom control you create utilizing the bascontrol_ns module.

* This controller sits on a Raspberry Pi. I currently have one running along with Polyglot on the RPI making it a stand alone controller so you can easily add it to your ISY.

* To use as stand alone Use UXTERM: This to Auto and Delay start of Polyglot in terminal on reboot to allow BASpi to Startup First!
Commands: Install; sudo apt-get install xterm
Add working Directory; mkdir -p ~/.config/autostart
Edit Start file; sudo nano ~/.config/autostart/lxterm-autostart.desktop
* UXTERM Auto Start Script

* [Desktop Entry]

* Encoding=UTF-8

* Name=Terminal autostart

* Comment=Start a terminal and list directory

* Exec=/usr/bin/lxterm -e 'cd /home/pi'

* Exec=/usr/bin/lxterm -e 'NODE_ENV=development ./polyglot-v2-linux-armv7’

#### Future

* Need to somehow add pulldown for the Universal Inputs. The universal inputs have a large list of configurable UOM's of their own.
Please see configuration quick start link above. On page two, 2 it shows the GUI for the device there you can pick on each universal input to configure its type, a seperate UOM. Also see the viedo below.

![Future Adds](https://github.com/sjpbailey/UDI-BASpi-SYS6U6R-master/blob/master/Images%2Fshot_3.png)

[Universal Input Configuration Viedo](https://www.youtube.com/watch?v=hTd1mR7npP4)

* Python 3.7.7

* Supported Nodes
  * Six 6 Universal Inputs
  * Six 6 Binary Outputs
  
##### Configuration

* requirments
* bascontrolns==0.0.3
* certifi==2020.11.8
* chardet==3.0.4
* idna==2.10
* markdown2==2.3.10
* netifaces==0.10.9
* paho-mqtt==1.5.1
* polyinterface==2.1.0
* python-dotenv==0.15.0
* requests==2.25.0
* urllib3==1.26.2

###### Defaults

* Default Short Poll:  Every 60 seconds
* Default Long Poll: Every 4 minutes (heartbeat)
* requirments unreleased bascontrol_ns module

###### User Provided

* Enter your IP address for your BASpi-SYS6U6R controller,
* key = baspi6u6r_ip Value = Enter Your BASpi IP Address.
* Save and restart the NodeServer
* sjb

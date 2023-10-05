# easyDCP Player+ Remote Control
[easyDCP Player+](https://www.easydcp.com), powered by [Fraunhofer IIS](http://www.iis.fraunhofer.de), is the leading software for digital cinema content playback on standard PC and Mac.  
This **free and open-source** extension allows you to remotely control the easyDCP Player+ software.

*easyDCP Player+ Remote Control* consists of two software components:
- a **server application** running on the computer together with easyDCP Player+
- a **progressive web application (PWA)** running on any device in a web browser

### Server Application
The server application acts as a bridge between easyDCP Player+ and PWA.
Therefore, it must be installed on the same computer together with easyDCP Player+.  
The server application controls the graphical user interface (GUI) of the easyDCP Player+ software by simulating keyboard input and mouse click events.
Additionally, the PWA is hosted via an integrated web server.
A RESTful-API and WebSockets are used for communication between server application and PWA.

### Progressive Web Application (PWA)
For best platform compatibility the user control is implemented as a progressive web application (PWA).
You can run the PWA on any device with a modern web browser.
After the server application is running connect the PWA with the correct server IP address and port number and start controlling the easyDCP Player+ software remotely.  
Below you see some mockups of the PWA:  
![easyDCP Player+ Remote Control PWA control dashboard mockup](/Impressions/mockup_control-dashboard.png "Control Dashboard") ![easyDCP Player+ Remote Control PWA connection settings mockup](/Impressions/mockup_connection-settings.png "Connection Settings")

## Application Requirements
The server application requires [.NET 7 or later](https://dotnet.microsoft.com/download) on a PC or Mac.  
The PWA can run in any modern web browser on any device.  
Both devices (computer with server application and device running the PWA) must be connected to the same local network in order to communicate.

## Manual
1. Make sure the correct *.NET* version is installed on the computer.  
For more information see the [application requirements](#application-requirements).
2. Run *easyDCP Player+*.
3. Run *easyDCP Player+ Remote Control - Server*.
    1. Configure the server application.
    2. Set the button coordinates for *easyDCP Player+*.
5. Open the PWA
    1. Make sure your device is connected to the same local network than the computer running the server application.
    2. Open your web browser.
    3. In the address bar type `http://[IP]:[port]` according to your server settings (e.g. `http://192.168.178.10:8080`).
    4. Configure the PWA.
    5. Connect to your server.

## Development
This software was developed with [Visual Studio Community 2022](https://visualstudio.microsoft.com/).  
The server application is written in *C#* and based on *.NET 7*, *ASP.NET* and *.NET MAUI*.  
The PWA is written in *HTML*, *CSS* and *JavaScript*. 

## Copyright
This software was invented and developed by [Sebastian Lang](https://sebastianlang.net).  
Copyright © 2023 Sebastian Lang.

## License
The software is licensed under [MIT licence](https://opensource.org/license/mit).  
For more information see the [license file of this repository](/LICENSE).

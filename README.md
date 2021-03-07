<p align="center"><img src="https://spportcovid19patient.000webhostapp.com/DIpuNTI.jpg"></p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3-brightgreen.svg?style=plastic">
<img src="https://img.shields.io/badge/Docker-✔-blue.svg?style=plastic">
</p>

<p align="center">
  <a href="https://twitter.com/jeopardy4u"><b>Twitter</b></a>
  <span> - </span>
  <a href="https://instagram.com/loathfaith"><b>Instagram</b></a>
  <span> - </span>
  <a href="https://github.com/loathsomeguy"><b>Tej's Page</b></a>
</p>

<p align="center">
  <br>
  <b>Available in</b>
  <br>
  <img src="https://i.imgur.com/1wJVDV5.png">
</p>

Concept behind Seeker is simple, just like we host phishing pages to get credentials why not host a fake page that requests your location like many popular location based websites. Contact for more on <a href="https://instagram.com/loathfaith"> Tej's Page </a>.Seeker Hosts a fake website on **In Built PHP Server** and uses **NGROK** to generate a link which we will forward to the target, website asks for Location Permission and if the target allows it, we can get :

* Longitude
* Latitude
* Accuracy
* Altitude - Not always available
* Direction - Only available if user is moving
* Speed - Only available if user is moving

Along with Location Information we also get **Device Information** without any permissions :

* Operating System
* Platform
* Number of CPU Cores
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* IP Address Reconnaissance

**This tool is a Proof of Concept and is for Educational Purposes Only, Seeker shows what data a malicious website can gather about you and your devices and why you should not click on random links and allow critical permissions such as Location etc.**

## How is this Different from IP GeoLocation

* Other tools and services offer IP Geolocation which is NOT accurate at all and does not give location of the target instead it is the approximate location of the ISP.

* Seeker uses HTML API and gets Location Permission and then grabs Longitude and Latitude using GPS Hardware which is present in the device, so Seeker works best with Smartphones, if the GPS Hardware is not present, such as on a Laptop, Seeker fallbacks to IP Geolocation or it will look for Cached Coordinates.  

* Generally if a user accepts location permsission, Accuracy of the information recieved is **accurate to approximately 30 meters**, Accuracy Depends on the Device.

**Note** : On iPhone due to some reason location accuracy is approximately 65 meters.

## Templates

You can choose a template which will be used by seeker from these : 

* NearYou
* Google Drive
* WhatsApp 
* Telegram

## Tested On :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Kali Nethunter
* Termux
* Parrot OS

## Installation

### Kali Linux / Ubuntu / Parrot OS

```bash
git clone https://github.com/loathsomeguy/seeker.git
cd seeker/
chmod 777 install.sh
./install.sh
```

### BlackArch Linux

```bash
pacman -S seeker
```

### Termux

```bash
git clone https://github.com/loathsomeguy/seeker.git
cd seeker/
chmod 777 termux_install.sh
chmod 777 ngrok
./termux_install.sh
```

## Usage

```bash
# In First Terminal Start seeker in Manual mode like this
python3 seeker.py -t manual

# In Second Terminal Start Ngrok or any other tunnel service on port 8080
./ngrok http 8080
```

## Photo upload path for WhatsApp group would be
```bash
/storage/emulated/0/Download/images.png
```
## Known Problems

* Services like Serveo and Ngrok are banned in some countries, In India Ngrok is working. so if it is banned in your country you may not get a URL, if not then first READ CLOSED ISSUES, if your problem is not listed, create a new issue.

## Warning
***This tool is only for educational purpose. If you use this tool for other purposes except education we will not be responsible in such cases.***

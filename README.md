# Phishing with ESP8266 (Google Phishing Page)

This is a Arduino script to host wifi network using ESP8266 which would work as a phishing page. When a user connects to this wifi network with your preffered SSID 
They would be redirected to login into the wifi as most commercial wifi networks do. But this login page is for Google Gmail, and once the user submits the credentials
they are stored in the ESP8266 for the attacker to view later. After submitting the credentials successfully the user would be shown a "Connected" page but there would 
be no network access as the ESP8266 does not have any network access.

TL;DR

This is a phishing page of Google Gmail with ESP8266.

## Preview

|                                                 Login  Wifi                                                                       |                                           Submitted Successfully                                                              |                               View Credentials                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| <img src="https://github.com/user-attachments/assets/7e2f86fa-166b-4b6c-b4d2-75096792337b" width="280"/> | <img src="https://github.com/user-attachments/assets/4ee7fc4f-7901-438d-956a-c6367d4ed755" width="280"/> | <img src="https://github.com/user-attachments/assets/12dd4cc3-6103-4cb2-9c8d-1fd8b3deac26" width="280"/> |

# Setup

- Install Arduino IDE from [official website](https://www.arduino.cc/en/software#legacy-ide-18x) (You need Arduino IDE version 1.8.X to upload file system)
- Install required libraries and dependencies for ESP8266 ([Guide](https://randomnerdtutorials.com/how-to-install-esp8266-board-arduino-ide))
- Install [SPIFFS tool](https://www.instructables.com/Using-ESP8266-SPIFFS/#step2) for ESP8266
- Clone this repo
  ```
  git clone https://github.com/Wraient/Google-Phishing-with-ESP8266
  ```
- Open `esp8266_phishing.ino` and change SSID
- Copy `index.html` in your data folder or copy `data/` in your Arduino project root
- Flash SPIFFS
- Flash script
- Connect to the wifi network and navigate to `connectivitycheck.gstatic.com/getinfo` on an Android or `http://www.msftconnecttest.com/getinfo` on Windows to see your collected passwords
- Navigate to `baseurl/deleteinfo` if you want to clear all the collected passwords
- Profit ????

P.S. Yes all the links on the page works.

*Only for educational purposes ofc. Have fun skids. 

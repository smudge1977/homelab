# Home Assistant automation

Used a proxmox automation script to do the install.  
Connected the the zwav on the pi for rad temp readings.

url | user | password
---|---|---|
http://192.168.0.132:8123/ | keith | letmein123!  


##  Mosquitto broker

mqtt_user letmein123! can only logon from local network
this is what the plugs mqtt will then use

## Flashing WiFi plugs
```
git clone https://github.com/ct-Open-Source/tuya-convert.git
sudo ./install_prereq.sh
sudo ./start_flash.sh
```
Plug at http://192.168.4.1  
Setup to my WiFi and do firmware update  

Configuration other and put in codes for GPIO stuff  
Configure - Other configuation string:  
```
{"NAME":"Gosund UP111","GPIO":[0,320,0,32,2720,2656,0,0,2624,576,224,0,0,0],"FLAG":0,"BASE":18}
```

After setting up MQTT broker details in plug

Switch MQTT data on from plugs console:  
```
SetOption19 on
```

https://www.youtube.com/watch?v=ITNDp2Rk_Ac
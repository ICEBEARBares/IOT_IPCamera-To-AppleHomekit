# **IP Camera > Apple Homekit**
###### > This Project Is The Useful Article To Someone Who Wanna Add Their IP Cameras Into The Apple Homekit.

# **"STEPS"**
### 1. Install The "Homebridge OS" From [This Link](https://homebridge.io/) & [Here's The Totorial To Install](https://github.com/homebridge/homebridge/wiki) .
###### > By the way , This Project Will Use The Raspberry Pi 4 (4GB Model).
<img src="https://user-images.githubusercontent.com/105172693/187125375-f6cb4c15-a0b5-47aa-a4fa-a78c60194d47.png" width=40% height=40%>

### 2. Then Finding The IP Of Your Local Platform Server & Setting Up The Homebridge Via The IP Address
###### > You Can Find The IP Adress Via Router From This IP , [192.168.1.1](192.168.1.1) & Access By Website Browser
### 3. Once , When You're Done By Setting Up The Account And Ready. It Will Be Look Like This
![image](https://user-images.githubusercontent.com/105172693/187121012-3ad031f5-cd92-4819-9820-a9e9eaa95822.png)
### 4. In Plugins Section , Go There & Serching This Plugin & Install
![image](https://user-images.githubusercontent.com/105172693/187124064-b74ed4e6-206b-4cff-8ffa-3784985b03d1.png)

```
Homebridge Camera Ui
```
### > Make Sure That The Plugin's Appear
![image](https://user-images.githubusercontent.com/105172693/187121612-f02d7b18-e1fb-4fd1-9f35-e69ccdac68d1.png)
### 5. To Adding The Camera , Press Setting > Config > Camera
<img src="https://user-images.githubusercontent.com/105172693/187121825-5175e6e5-8269-4a95-a740-7bc101b09325.png" width=40% height=40%>

### 6. Then Finding The "RTSP Address" To Place It Into The Homebridge In Stream Configuration Section , [Here](https://www.nellyssecurity.com/blog/articles/video-surveillance/how-to-find-your-cameras-rtsp-address#:~:text=If%20you're%20looking%20at,media%2Fvideo%5BSTREAM%20TYPE%5D)

<img src="https://user-images.githubusercontent.com/105172693/187122356-92608736-1ee9-43a1-8b3f-3fadb999a381.png" width=40% height=40%>


### - The Example Of The Camera Configuration
```
"cameras": [
                {
                    "name": "Primary DVR - Front",
                    "manufacturer": "imou",
                    "model": "Bullet 4MP",
                    "serialNumber": "0",
                    "motion": true,
                    "motionTimeout": 15,
                    "unbridge": true,
                    "hsv": false,
                    "prebuffering": false,
                    "prebufferLength": 8,
                    "videoConfig": {
                        "source": "-i rtsp://admin:admin@192.168.1.90/cam/realmonitor?channel=1&subtype=01",
                        "subSource": "-i rtsp://admin:admin@192.168.1.90/cam/realmonitor?channel=1&subtype=01",
                        "stillImageSource": "-i rtsp://admin:admin@192.168.1.90/cam/realmonitor?channel=1&subtype=01",
                        "rtspTransport": "tcp",
                        "maxWidth": 0,
                        "maxHeight": 0,
                        "maxFPS": 0,
                        "maxBitrate": 5000,
                        "forceMax": true,
                        "vcodec": "copy",
                        "acodec": "libfdk_aac",
                        "audio": true,
                        "debug": true
                    },
```  
### 7. To Adding To The Apple Homekit System Use Your Device To Scan The QR Code At The Home Page Of The Homebridge , Then Follow The Steps In Your Device
<img src="https://user-images.githubusercontent.com/105172693/187123586-cb313ed1-2b23-4c81-9ba2-a6ca81bfd4dc.jpg" width=25% height=25%>

### 8. Here's The Result

![Genki Arcade - 2022-08-29 044348](https://user-images.githubusercontent.com/105172693/187124684-faf8e1ed-ba03-4492-a106-82335288e9ec.jpg)
###### > Apple TV 4K As The Local Home Hub




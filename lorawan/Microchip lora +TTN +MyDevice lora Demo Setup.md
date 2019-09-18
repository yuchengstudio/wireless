#                                          Microchip + TTN + MyDevices LoRa Demo Setup
## 1.lorawan应用的组成结构
众所周知，整个LoRaWAN系统由终端设备，网关，网络服务器和应用服务器组成。 LoRaWAN物理拓扑可以如下图所示。
![image](https://github.com/yuchengstudio/wireless/blob/master/lorawan/reference/microchip_lora_ttn_001.png)
<br/>在本演示中，我们将使用DV164140-1的最终器件Microchip DM164138或Mote板，Microchip Gateway EVK DV164140-1，thethingsnetwork Network Server和MyDevices Application Server。

## 2.Preparations
### 1.1 Hardware Preparations:
#### 1.1.1 DV164140-1 including Microchip LoRa Mote, and an 8-channel Gateway
#### 1.1.2 A router which can connect to internet/cloud
### 1.2 Software Preparations:
#### 1.2.1 LoRaDevUtility for LoRa Mote and Gateway configuration
#### 1.2.2 Create an account in https://console.thethingsnetwork.org/
#### 1.2.3 Create an account in https://mydevices.com/

## 3.Connect Microchip LoRawan mote to TNN
### 3.1 Setup the Gateway Hardware
#### 3.1.1 Connect the Gateway Radio Board to the Gateway Core Board.
#### 3.1.2 Connect the antenna to the Gateway Radio Board.
#### 3.1.3 Connect an Ethernet cable from your router to the Ethernet jack on the Core Board.
#### 3.1.4 Connect a micro USB cable from computer to the USB jack on the Gateway Core Board.This will be used to configure the Gateway through the LoRaDevUtility.
#### 3.1.5 Install the micro SD card into the slot on the Gateway Core Board. This card is used to store the Gateway parameters.
![image](https://github.com/yuchengstudio/wireless/blob/master/lorawan/reference/microchip_lora_ttn_002.jpg)

## 3.2 Configure the Gateway Parameters
<br/>3.2.1 In the “Core Board Setup” section, select “DHCP” for the IP Allocation Mode.
<br/>3.2.2 In the “Server Setup” section, set your LoRa Server IP to the TTN server. You can find the
correct address here:
https://www.thethingsnetwork.org/wiki/Backend/Connect/Gateway#connect-a-gateway
_server-addresses
For the EU, it is router.eu.thethings.network or 52.169.76.203. Since the IP address is
required, but may change over time, you should check the hostname on an IP resolver
site like http://whatismyipaddress.com/hostname-ip
<br/>3.2.3 In the “General Actions” section, click the “Save Settings to SD Card” button
<br/>Once you have completed these steps, you should see in the LoRaDevUtility software that you
are “Online”. If it is not online, you may need to enable enable Port Forwarding in your router to
open up the port 1700. Or sometimes, you may need to restart the router, the Gateway and the
LoRaDevUtility, and try it again.



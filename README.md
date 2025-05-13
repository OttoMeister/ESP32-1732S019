# ESP32-1732S019
ESP32-1732S019 ARDUINO ESP32-S3, 1,9 zoll 170*320 

![ESP32-1732S019](https://github.com/OttoMeister/ESP32-1732S019/assets/12480979/2e7e7fbe-8a32-4804-abf7-d8c90f59159e)

## General Information
[Aliexpress 1](https://www.aliexpress.us/item/3256806186900969.html) , 
[Aliexpress 2](https://www.aliexpress.us/item/3256806071867483.html) ,
[Aliexpress 3](https://www.aliexpress.us/item/3256806436770867.html) <br>
https://www.surenoo.com/products/23377371?utm_source=chatgpt.com
<br><br>
Thanks to the efforts of these individuals and many others, programming on Suntown displays has become very easy. 
<br><br>
https://github.com/rzeldent/esp32-smartdisplay<br>
https://github.com/rzeldent/platformio-espressif32-sunton<br>
https://github.com/lvgl/lv_port_esp32<br>
https://github.com/platformio/platformio-core<br>
https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display<br>
<br>
Here, I used the ESP32-1732S019 to create a small demo project featuring WiFi, METAR (Meteorological Aerodrome Report) weather data, and NTP time. 

## Install PlatformIO on Linux (no IDE)
```
curl -fsSL -o get-platformio.py https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py
python3 get-platformio.py
curl -fsSL https://raw.githubusercontent.com/platformio/platformio-core/develop/platformio/assets/system/99-platformio-udev.rules | sudo tee /etc/udev/rules.d/99-platformio-udev.rules
sudo service udev restart
export PATH=$PATH:$HOME/.local/bin
ln -s ~/.platformio/penv/bin/platformio ~/.local/bin/platformio
ln -s ~/.platformio/penv/bin/pio ~/.local/bin/pio
ln -s ~/.platformio/penv/bin/piodebuggdb ~/.local/bin/piodebuggdb
pio settings set enable_telemetry no
pio settings set check_platformio_interval 9999
```
## Compile with PlatformIO on Linux
```
git clone https://github.com/OttoMeister/ESP32-1732S019
cd ESP32-1732S019/
platformio run 
platformio run --upload-port  /dev/ttyUSB0 -t upload
platformio run --monitor-port /dev/ttyUSB0 -t monitor
```
## Install PlatformIO on Win10-11 (no IDE)
Windows Command Prompt <br>
Install Python:
```
winget install Python.Python.3.13
REM Restart Windows Command Prompt 
python -V
python.exe -m pip install --upgrade pip
```
Install Git:
```
winget install git.git
REM restart Windows Command Prompt 
git --version
```
Install PlatformIO:
```
pip install platformio
pio --version
pio settings set enable_telemetry no
pio settings set check_platformio_interval 9999
```
Install CP210x driver:
```
cd %USERPROFILE%\Desktop
curl -L --fail -o cp210x.zip https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip --silent
mkdir cp210x
tar -xf cp210x.zip -C cp210x
start /wait cp210x\CP210xVCPInstaller_x64.exe /S
```
Install CH340 (WCH) driver:
```
cd %USERPROFILE%\Desktop
curl -L --fail -o CH341SER.exe https://www.wch.cn/download/file?id=65  --silent
start /wait CH341SER.exe /S
```
## Compile with PlatformIO on Win10-11
```
cd %USERPROFILE%\Desktop
git clone https://github.com/OttoMeister/ESP32-1732S019
cd ESP32-1732S019/
platformio run 
platformio run --upload-port  COM1 -t upload
platformio run --monitor-port COM1 -t monitor
```


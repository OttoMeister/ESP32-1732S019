# ESP32-1732S019
ESP32-1732S019 ARDUINO IDE 2.3.2 ESP32-S3, 1,9 zoll 170*320 

![ESP32-1732S019](https://github.com/OttoMeister/ESP32-1732S019/assets/12480979/2e7e7fbe-8a32-4804-abf7-d8c90f59159e)

## General Information
[Aliexpress 1](https://www.aliexpress.us/item/3256806186900969.html) , 
[Aliexpress 2](https://www.aliexpress.us/item/3256806071867483.html) ,
[Aliexpress 3](https://www.aliexpress.us/item/3256806436770867.html) <br>

## How to install ARDUINO IDE 2.0.3 with ESP32 support on Windows

Open BoardManger and install ESP32 by Espressif (2.0.11)
Select "ESP32-S3 Dev Board" in your bord selection.

Install librarys:
```
#include <TFT_eSPI.h>     // by Bodmer ver 2.5.43
#include <NTPClient.h>    // by F.Weinberg ver 3.2.1
#include <HTTPClient.h>   // by A.McEwen ver 2.2.0
#include <ArduinoJson.h>  // by B.Blanchon ver 7.0.3
```
Copy this in "~/Arduino/libraries/TFT_eSPI/User_Setup.h" or
"C:\Users\YOR_USER_NAME\Documents\Arduino\libraries\TFT_eSPI\User_Setup.h"
```
#define ST7789_DRIVER  
#define TFT_WIDTH 170
#define TFT_HEIGHT 320
#define TFT_MISO -1 
#define TFT_MOSI 13   
#define TFT_SCLK 12
#define TFT_CS   10 
#define TFT_DC   11 
#define TFT_RST  1 
#define TFT_BL   14
#define TFT_BACKLIGHT_ON HIGH
#define LOAD_GLCD  
#define LOAD_FONT2 
#define LOAD_FONT4 
#define LOAD_FONT6 
#define LOAD_FONT7
#define LOAD_FONT8 
#define LOAD_GFXFF 
#define SMOOTH_FONT
#define SPI_FREQUENCY  40000000
```









# FLsun I3 Marlin Configuration
This repository have the configuration files for Flsun i3 printer used on **Marlin 2.0.7** firmware. The configuration files can be used with either autolevel sensor or endstop switch. Configuration files for old versions also kept in **'Old_Versions'** folder.



 <img src="flsun.jpg" alt="Flsun" style="zoom:50%;" />



### Sensor Type



This configuration files are setted for the PNP type proximity sensor however the type of the sensor came along with the printer is NPN therefore if wanted to use issued sensor the following changes need to be made in the **'Configuration.h'** file.

```c++
#define Z_MIN_ENDSTOP_INVERTING false
#define Z_MIN_PROBE_ENDSTOP_INVERTING true 
```

 

### Using The Configuration Files

This configuration files must be used with [Marlin](https://github.com/MarlinFirmware/Marlin) firmware. 



After cloning or downloading the Marlin repository, **"Configuration.h"** and **"Configuration_adv.h"** files in the Marlin folder need to be changed with the files in this repository.



### Uploading The Firmware

Firmware can be uploaded using either PlatformIO or Arduino IDE. 



#### For PlatformIO 

Be sure the compile environment is correct in **'platformio.ini'** file. For MKS Gen L 1.0 have to be like that :

```ini
[platformio]
default_envs = mega2560
```



After that just check the COM port and press Upload All button.



#### For Arduino IDE

Open 'Marlin/Marlin/Marlin.ino' file in Arduino IDE. Select 'Mega 2560' board and the correct COM port then press the Upload button.
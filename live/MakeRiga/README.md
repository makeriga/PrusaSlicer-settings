# Adding vendor config manually
You will need to do some manual steps in order to activate these new system profiles. First of all you need to find the config folder. 
The possible configuration locations are:
 * MacOS `~/Library/Application Support/PrusaSlicer`
 * Windows `C:/Users/username/AppData/Roaming/PrusaSlicer.`
 * Linux `~/.config/PrusaSlicer`

## Add vendor configuration to your local config
Create a file named MakeRiga.ini under `./PrusaSlicer/vendor` and add the latest version of [MakeRiga config](https://github.com/makeriga/PrusaSlicer-settings/tree/master/live/MakeRiga) into the `./PrusaSlicer/vendor/MakeRiga.ini` file.

## Add the printer to local config
To configure the PrusaSlicer you need to provide details how to modify PrusaSlicer.ini that is located in configuration folder by adding this section.

`./PrusaSlicer/PrusaSlicer.ini`
```ini
[vendor:MakeRiga]
model:MRNEPTUNE2 = 0.4;0.6;0.8
```


Add these filaments to the `[filaments]` section:

`./PrusaSlicer/PrusaSlicer.ini`
```ini
[filaments]
...
Generic ABS @MRELEGOO = 1
Generic PETG @MRELEGOO = 1
Generic PLA @MRELEGOO = 1
```

## Update to latest config
To update the vendor config you will need to 
1. Close PrusaSlicer
2. Copy the latest version of [MakeRiga config](https://github.com/makeriga/PrusaSlicer-settings/tree/master/live/MakeRiga) into the `./PrusaSlicer/vendor/MakeRiga.ini` file
3. Reopen PrusaSlicer
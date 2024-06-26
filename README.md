1) Instructions:

```
git clone https://github.com/micropython/micropython.git
cd micropython/ports/stm32/boards

git clone https://github.com/knoppixmeister/Micropython-WeAct-F405RGT6-Port.git WeAct-F405RG

make BOARD=WeAct-F405RG submodules
make BOARD=WeAct-F405RG

cd build-WeAct-F405RG
```

2) Optional:
```
ls -lah | grep firm
```

3) Flash .hex file to the board by STM32CubeProgrammer
```
1) Boot the board in DFU mode holding B0 button while plug in to USB port. Release B0 button after 1 sec.
2) Start STM32CubeProgrammer. Select USB connection -> press Connect button
3) On the "Erase & programmimg" tabl (from left side) press "Full chip erase". Wait for proess complete 
4) Go Back to "Memory & File editing" tab. Click "Open File" tab (from top). Find and open created .hex file from step 1 & 2
5) Click "Download" button. Wait for process until completed.
6) Reconnect usb wire
```

4) Check result by opening some terminal app
```
minicom -D /dev/ttyACM0

screen /dev/ttyACM0

picocom /dev/ttyACM0
```

5) Enjoy!

Code borrowed form: https://github.com/WeActStudio/WeActStudio.STM32F4_64Pin_CoreBoard/tree/master/Examples/STM32F405/mpy/WeActStudio_F405RG

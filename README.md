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

4) Enjoy!

Code borrowed form: https://github.com/WeActStudio/WeActStudio.STM32F4_64Pin_CoreBoard/tree/master/Examples/STM32F405/mpy/WeActStudio_F405RG
